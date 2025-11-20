# Joystream CDN performance - part 1

2023-12-11

# Intro

We’ve had reports about users having trouble playing videos in Gleev for quite a while. To help the investigation, a “benchmark” of Joystream CDN was created. In this post I will share some of the analysis of the results, along with some observations and recommendations.

In this first section I will explain the test’s methodology in detail so that any issues with my approach can be spotted and pointed out. In the second section I will get to the actual results analysis. In the last section, I will discuss conclusions and recommendations.

This document will be the first part of analysis of CDN performance. In a later document I will take a look at the results of synthetic tests and possibly Atlas-related issues.

## Goals

This benchmark had a specific purpose: see how distribution performance is perceived by end users. While synthetic tests ran from data centres can help us understand the performance of our network, what ultimately matters is what the end (Gleev) user experiences. To best isolate the performance of the distribution network, for this test, only cached assets are considered. To get a full understanding of the storage system, that is not enough, but for now we focus strictly on performance of distributors. In the future we may want to run a similar test with uncached assets to get the full picture.

## Test methodology

The benchmark is a web application available at [https://benchmark.joyutils.org](https://benchmark.joyutils.org/). When ran, the test proceeds as follows:

1. Reference speed test is performed using Cloudflare - this allows us to normalize the download speeds and reduce impact of bad network connections on overall results, more on that later.
2. Test URLs are collected - details about both media and thumbnail data objects for the test video are fetched from the Query Node. Both objects will be downloaded from all operators so we get 18 test URLs (2 objects * 9 operators).
3. For each test URL a test is performed:
    1. In case of images, full image is downloaded and various measurements are taken - most notably full response time and time-to-first-byte (TTFB).
    In case of media, first 10/25 MB of the video are downloaded (using `bytes=0-${maxDownloadSize - 1}` Range header). As with images, full response time and TTFB are measured, but also download time (excluding initial connection) and download bandwidth.
    2. We wait 200ms to start the next run fresh.
    3. Both steps above are repeated 3 times. From those 3 runs, all the measurements are averaged and considered the final result for the given test URL.
4. After all URLs are tested, the results are sent to Elasticsearch for analysis. Each test URL with its measurements creates a single document.

### Normalized speeds

One thing that I was trying to avoid was poor network connections affecting the results. If we had a lot of users with a slow connection (like 15 Mbps) run the test, that could give us a fake impression that our infra offers slow download speeds, when in reality the values would be limited by users’ connection. To minimze impact of this, I’ve introduced `normalizedDownloadSpeed = downloadSpeed / referenceDownloadSpeed`, basically a ratio of utilization of user’s connection. `normalizedDownloadSpeed = 1` indicates that user was able to download with their full available speed from a given node. It’s not an ideal statistic and should be considered alongside unscaled download speeds.

### Test regions

For the purpose of analysis, I’ve split the results into multiple key regions. Most regions are just the continent, but Asia was split into more regions to give us better understanding of results across usage clusters:

1. South Asia - country is one of (India, Bangladesh, Nepal, Bhutan, Myanmar).
2. Southeast Asia - country is not one of the above and geo longitude is above 90 (includes Japan).
3. West Asia - all the remaining Asia results.

### `gateway.joyutils.org`

In the results analysis, you will see `gateway.joutils.org` ”node” which isn’t actually a real node and doesn’t actively participate in distribution at the moment. This URL points to a [Cloudflare Worker](https://workers.cloudflare.com/) which does only a single thing - proxies the request to `dist1.joyutils.org` which is a real node located in Germany. So if you send the request to `dist1.joyutils.org` or `gateway.joyutils.org`, the request will be handled by `dist1.joyutils.org` anyway. The only difference, as I understand it, is the network path the request has to travel. Let’s assume someone from Japan sends a request:

- Request sent directly to `dist1.joyutils.org` will travel over public networks to Germany.
- Request sent to `gateway.joyutils.org` will travel over public network only to the closest Cloudflare data centre to the user (most likely in Japan). Worker code will be executed there and will proxy a request to `dist1.joyutils.org` over Cloudflare’s private network. Most likely the request will use their private network up to Germany where it will travel the last mile over public network.

Given the fact that the request has to go to Germany anyway, I didn’t expect much impact on the performance but as you will find below, that was an incorrect assumption.

## Analysis Jupyter Notebook

All the following data was computed based on raw results from Elasticsearch. You can find the full Jupyter Notebook here: [https://github.com/joyutils/dwg-benchmark-jupyter/blob/main/benchmarks.ipynb](https://github.com/joyutils/dwg-benchmark-jupyter/blob/main/benchmarks.ipynb) This code fetches the results, transforms them and produces most of the graphs.

# Results

Thanks to efforts of marketing and human resources work groups, we’ve collected over 200 results over 2 weeks from 130 users, from all (populated) continents. Below you can see geographical distribution of results:

![CleanShot 2023-12-08 at 12.20.20@2x.png](Joystream%20CDN%20performance%20-%20part%201/CleanShot_2023-12-08_at_12.20.202x.png)

![tests_per_region.png](Joystream%20CDN%20performance%20-%20part%201/tests_per_region.png)

For context, average reference download speeds and geo locations of all the nodes:

![avg_reference_speed.png](Joystream%20CDN%20performance%20-%20part%201/avg_reference_speed.png)

![CleanShot 2023-12-11 at 12.45.37@2x.png](Joystream%20CDN%20performance%20-%20part%201/CleanShot_2023-12-11_at_12.45.372x.png)

![CleanShot 2023-12-11 at 12.45.51@2x.png](Joystream%20CDN%20performance%20-%20part%201/CleanShot_2023-12-11_at_12.45.512x.png)

## Thumbnail downloads

First, let’s look at results for thumbnail image downloads. Here we’re considering the full request time, including initial connection and content download. Below you can see comparison between best available operator and the closest one geographically to the user.

![best_thumbnail_time.png](Joystream%20CDN%20performance%20-%20part%201/best_thumbnail_time.png)

![closest_thumbnail_time.png](Joystream%20CDN%20performance%20-%20part%201/closest_thumbnail_time.png)

Looking at best available operator, we can see satisfactory (below 300ms) values for all regions except Africa, Oceania and South America. This makes sense since we don’t have any nodes in those regions. 90th percentile of North America result is somewhat concerning, with 10% of images taking more than 1.3s to download.

When looking at results from the closest operator, we can see degradation of results with slightly higher medians and quite higher 90th percentile. Some increase in those values can be expected though, because with only a single operator considered, results will be more impacted by temporary slowdowns and network interruptions. Considering that only Africa and South America (regions in which we don’t currently have nodes) have medians above 500ms, I still consider those results satisfactory. However, difference between best and closest operator in Southeast Asia and West Asia, regions which should be well covered by our network, is quite considerable. To better understand those differences, let’s consider the full matrix of region↔operator values:

![heatmap_thumbnail.png](Joystream%20CDN%20performance%20-%20part%201/heatmap_thumbnail.png)

For Southeast Asia, best performance is offered by `distributor-node.mms.team`, located in Singapore, so also the closest node for all results excluding single test from Japan. That may suggest varying performance offered by this node.

In case of West Asia however, best performance is offered by `dist1.joyutils.org`, but the closest node geographically is actually `sieemmanodes.com` located in Ukraine. For users in West Asia, closest node is outperformed by 3 other European nodes.

## Video downloads

### Video bandwidth

Now let’s consider streaming of videos. First, we are considering the available download speed that will indicate the smoothness of video playback. For context, Full HD video requires around 5Mbps of bandwidth to play smoothly.

![best_media_speed.png](Joystream%20CDN%20performance%20-%20part%201/best_media_speed.png)

![best_media_speed_normalized.png](Joystream%20CDN%20performance%20-%20part%201/best_media_speed_normalized.png)

![closest_media_speed.png](Joystream%20CDN%20performance%20-%20part%201/closest_media_speed.png)

![closest_media_speed_normalized.png](Joystream%20CDN%20performance%20-%20part%201/closest_media_speed_normalized.png)

When considering best available operator, all regions offer sufficient streaming bandwidth, even considering the bottom 10th percentile. Only South Asia’s 10th percentile falls slightly below 5Mbps (at 4.4). However, only considering the closest operator, the results don’t look so great anymore. While medians still suggest good experience on average, Africa, South Asia and (weirdly) North America’s 10th percentiles are at around 1Mbps, which isn’t a great result. On average, users from Africa and South Asia don’t have great internet connections, with average reference download speed around 20Mbps, which certainly can impact the results here. Not sure where the low 10th percentile comes from in North America, that’s unexpected.

Looking at normalized speed from best operator, we can see that except South America, on average, our CDN offers decent utilization of user’s internet connection. Considering only the closest operator we see degradation of results again with median utilization across all regions at around 50%, which I still consider an acceptable result. 10th percentile values from the closest operator again suggest inconsistent performance.

For more context, let’s take a look at the full results:

![heatmap_media.png](Joystream%20CDN%20performance%20-%20part%201/heatmap_media.png)

![heatmap_media_normalized.png](Joystream%20CDN%20performance%20-%20part%201/heatmap_media_normalized.png)

Couple of observations here:

1. `gateway.joyutils.org` outperforms every other node in all regions except Oceania and Southeast Asia, which makes sense considering the vast distance to Germany. Globally, on average, it offers double the performance of its “base node”, `dist1.joyutils.org`.
2. The node we raised specifically to cover South Asia region, `dwg.joystream.name`, located in Mumbai, India, doesn’t offer great streaming performance in South Asia. It’s outperformed by the Tokyo node and also matched in performance by `distributor-node.mms.team`, located in Singapore.
3. In Southeast Asia region, we can see that the main node covering the region, `distributor-node.mms.team`, doesn’t offer great performance and is in fact outperformed 2x by the Tokyo node.
4. Africa has currently the worst streaming performance, especially if you exclude `gateway.joyutils.org`, which offers the best performance in the region but doesn’t participate in distribution.
5. In North America, the closest node, `nodelefrog.store`, is outperformed by one European node and the node in Tokyo. Another 3 European nodes are very close in performance.

### Video latency

Still looking at video downloads, let’s also consider another statistic, time-to-first-byte (TTFB). This indicates the time client needed to wait before they received any response, possibly indicating the “loading time”, before the playback even started.

![best_media_ttfb.png](Joystream%20CDN%20performance%20-%20part%201/best_media_ttfb.png)

![closest_media_ttfb.png](Joystream%20CDN%20performance%20-%20part%201/closest_media_ttfb.png)

Looking at the values themselves, I’d say for videos, they are satisfactory. Even considering only the closest operator, all regions have medians below 0.9s. 90th percentile gets as high as 1.7s for West Asia (which we’ve established above doesn’t get best performance from the closest node), possibly picking a different node for West Asia users would reduce those values.

Interestingly, TTFBs for videos are ~70-80% higher than time required for fetching an image, from the same region/provider. This suggests that most likely there’s considerable processing time on Argus side.

Full results for video TTFB:

![heatmap_media_ttfb.png](Joystream%20CDN%20performance%20-%20part%201/heatmap_media_ttfb.png)

1. `gateway.joyutils.org` on average has twice the latency of `dist1.joyutils.org`, even though it provides twice the bandwidth.
2. West Asia again is not best served by the closest node geographically.
3. Interestingly, lowest video latency in North America is actually offered by an European node. That’s not the case for image downloads though. If my previous hypothesis about non-trivial Argus processing times for videos is correct, this could suggest that our North American node (`nodelefrog.store`) doesn’t offer great processing performance and even with network latency head start, it still has worse overall latency than faster European node.
4. Considering video latency, `dwg.joystream.name` still doesn’t offer best performance in South Asia region, with the Singapore node having lower media latency.
5. In Southeast Asia, even though the closest node, `distributor-node.mms.team` doesn’t offer the best streaming performance, its media latency is the lowest.

# Conclusions

Considering all the results my conclusion is that the performance of our CDN across all regions is decent. While there’s certainly a ton of space for improvements, I don’t see any obvious, major issues. Below you can find some specific areas of improvements or further investigation that I think are worth considering.

### Bottom 10%

Some of the 10th/90th percentile values indicate inconsistent performance in some regions. 10th percentile of normalized download speed from the closest operator is below 0.1 in most regions, including Europe. That means bottom 10% of users only were able to utilize 10% of their max internet speed when downloading video, even in well connected regions.

Something that possibly could be an impact here are state cleanups that all Argus nodes periodically do (once 24h and at startup). When they are performed, QN is asked for all the objects in worker buckets. This is very unoptimized at the moment and when resolving this query, QN can take 100% of CPU usage for 20-30 minutes (sic!). It can be expected that any requests sent to a node under this load will take much longer to resolve. This probably doesn’t explain all the low results, but most likely is a factor.

### Geo distance vs performance

While we can see the general trend of latency going down as the geographical distance to the node goes down, that’s not always the case, especially for video latency. Also, we can see few examples of nodes offering better performance than the one closest to the user:

1. For users in North America, the node in North America (`nodelefrog.store`) is not very useful. While it offers slightly faster median image download times (331ms vs 454ms Japan and 480ms Germany), other nodes (Europe and Japan) offer both better video latency and video streaming bandwidth.
2. For South Asia users, the Indian node (`dwg.joystream.name`) is matched in image performance by the node in Singapore. It’s also outperformed by the Singapore node when it comes to media streaming and latency.
3. For Southeast Asia users, the closest node (`distributor-node.mms.team`) offers slightly better latency than the Tokyo node, but is vastly outperformed when it comes to streaming bandwidth.
4. For users in West Asia, the closest node (`sieemmanodes.com`) is not leading in any of the metrics, being outperformed by other European nodes in all categories.

### `gateway.joyutils.org`

As mentioned in the prior analysis, the experimental proxy node at `gateway.joyutils.org` offers a lot of bandwidth performance boost compared to its base node at `dist1.joyutils.org`. This highlights the importance of quality network connectivity for our nodes. The fact that this node can offer the best performance in almost all the regions just by leveraging Cloudflare network is quite astonishing. The downside is that the latency is on average twice as high, most likely caused by the processing time of the Cloudflare Worker.

### Redundant nodes?

For reference here’s the full list currently participating in distribution:

1. `nodelefrog.store` - North America, NYC
2. `jstrm.numisma.cc` - Europe, Netherlands
3. `dist1.joyutils.org` - Europe, Germany
4. `distributor.adovrn.xyz` - Europe, Russia (St. Petersburg) 
5. `sieemmanodes.com` - Europe, Ukraine
6. `dwg.joystream.name` - Asia, India
7. `distributor-node.mms.team` - Asia, Singapore
8. `tokyo.0x2bc.com` - Asia, Japan

Based on the results, I think some of those nodes are not really useful and potentially removing them could actually improve performance of our network:

1. `nodelefrog.store` - as previously mentioned, performance of this node is mostly matched or improved by nodes in Europe and Japan. Considering that you can actually get better performance by travelling additional few thousand kilometers, I think we should try finding another node in North America that offers better performance.
2. `dwg.joystream.node` raised specifically for South Asia users, gets outperformed by other Asian nodes in all metrics. I don’t see a good reason for keeping it around.
3. Historically, we’ve had a lot of usage coming in from Russia and Ukraine so we’ve made sure to have nodes in both of those countries to serve that demand. However, since quite some time that trend no longer holds and currently Russia and Ukraine are no longer in top 10 of users. Additionally, based on test results, other European nodes provide comparable performance for users in those regions:

![CleanShot 2023-12-11 at 14.56.35@2x.png](Joystream%20CDN%20performance%20-%20part%201/CleanShot_2023-12-11_at_14.56.352x.png)

![CleanShot 2023-12-11 at 14.56.59@2x.png](Joystream%20CDN%20performance%20-%20part%201/CleanShot_2023-12-11_at_14.56.592x.png)

Also, as pointed out before, the node in Ukraine gets selected as the closest node for West Asia users, even though it doesn’t provide best performance for them.

## Recommendations

*Note: Changes in node set won’t be applied until results are confirmed based on synthetic tests.*

1. Remove nodes:
    1. Remove `dwg.joystream.name` (India) as suggested above
    2. Remove `sieemmanodes.com` (Ukraine) or `distributor.adovrn.xyz` (Russia) or both
    3. Replace `nodelefrog.store` (USA) with another provider and possibly better performance
2. Add nodes:
    1. Add a node in South America to improve latency. Over last 15 days, South America had 2nd largest share of usage, with more usage than Europe.
    2. Consider adding a node in Africa following bad performance in that region. However, based on results average reference user speed in that region is below 20Mbps, so I’m not sure if we will be able to offer a good service there without optimized media (transcoding etc.).
3. Improve poor results for bottom 10%:
    1. Pray that Subsquid-based Argus comes soon so we get rid of crazy CPU usage 🙏
    2. Until gods answer, lower state cleanup even further, like once a week.
    3. Do stress-testing of Argus to see if the performance is consistent over longer period of time.
4. Look into how we can take advantage of Cloudflare network without the latency penalty. Obviously we shouldn’t over-rely on their services, but having 1-2 fast-connectivity nodes wouldn’t hurt.
5. We need proper review of how Atlas deals with operator selection. Its first choice is the node closest geographically, but there’s more (quite convoluted) logic and I’ve seen it do some funky things.
6. No matter how much we improve distribution, it will be challenging to offer good experience in regions with poor connectivity, like Africa or South Asia. We need to work on optimizing media for web streaming (transcoding, adaptive streaming, etc.) to properly serve users there.