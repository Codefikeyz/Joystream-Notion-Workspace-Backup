# Joystream CDN performance - part 2

# Intro

This part two aims at comparing result obtained in:

[Joystream CDN performance - part 1](Joystream%20CDN%20performance%20-%20part%201%20c8aff72f95ca4e86866079f81784aacb.md)

and verify its claims using data obtained via a ping script deployed across the globe.

Due to the low sample size for the user data benchmark it has been deemed necessary to compare results with a richer (but less geographically diverse) dataset coming from a ping script deployed in various locations across the globe. The data obtained through this “ping tool” is colloquially referred as synthetic data and the rationale behind this second report is:

<aside>
💡 if both the user data and the synthetic data confirm the same finding, then the information is considered accurate and action will be taken by the lead if necessary

</aside>

# Ping tool analysis

**Caveat**: the result reported refer to the **last 30 days** measurement

This is our current traffic in the past 30 days:

![Untitled.png](Joystream%20CDN%20performance%20-%20part%202/Untitled.png)

![Untitled 1.png](Joystream%20CDN%20performance%20-%20part%202/Untitled_1.png)

### Breakdown by top countries:

The cumulative traffic of the countries constitutes around 80% or more of the traffic for the continent

- Asia:
    - Bangladesh
    - Indonesia
    - India
- South America:
    - Venezuela
    - Argentina
    - Brazil
    - Colombia
- Europe
    - Finland
    - Russia
    - West Europe (Spain, France, Germany, Italy, UK…)
- North America:
    - US
    - Mexico

### Node performance vs Geolocation

The following result were obtained by deploying a script that fetches image `1343` and video `552149` In particular every one hour the image is fetched 5 times and the video 1. The script has been deployed in the following region via [google cloud scheduler](https://cloud.google.com/compute/docs/regions-zones) and ohv

- Europe
- Asia:
    - South Asia
    - Southeast Asia
    - NorthWest Asia
- US: east + west
- South America east

![Untitled 2.png](Joystream%20CDN%20performance%20-%20part%202/Untitled_2.png)

The role of this test is to reach a definitive conclusion on the data collected from user benchmark.

I will comment only on the suggestion concerning changing (adding or removing) the geolocation setup of the distributor nodes:

## Benchmark setup

The following sequence is performed ([reference](https://github.com/joyutils/dwg-tools/blob/d0253de56621e464250e05a367d310db1e1b3c3b/packages/dwg-utils/src/assetBenchmark.ts#L77)):

1. Client issues a `fetch` request at timestamp `startFetch`
2. Client receives the first byte of the response at timestamp `startResponse`
3. Client issues one or more `read` in order to fetch the full file, each round obtaining `maxDownloadBytes` bytes.
4. Client finishes receives all the `totalBytes` at timestamp `endFetch`

Assets fetches are of two types: image with id `1343` and video with id `552149` In particular every one hour the image is fetched 5 times and the video 1

## Benchmark metrics

The following metrics are considered

- **Bandwidth**: `totalBytes * 8 / ((endFetch - startResponse) * 1000)` ( the `8/1000` scaling factor is introduced since we want the result in Megabits per second, Mbps). This quantity is also called Download speed. The higher the bandwidth the smoother the streaming at high resolution. For a 4K video a value above 50 Mbps is ideal
- **Latency**: `startResponse - startFetch`, this quantity is measured as the time to first byte (TTFB). The lower the latency the better. Below 300 ms is considered adequate and below 150ms very good. The latency for image assets is effectively the same as the time taken for the first round of fetch since image size is usually below `maxDownloadBytes`. The latency measured for video assets includes extra overhead time taken by the Argus node for processing (user data benchmarks reveals a 70-80% overhead increase). I will distinguish the measurements for the 2 types of asset using terms “image latency” and “video latency”

## Node to be Retired

- Retire the node in NYC, the report suggest the following:
    - Video **Latency**: node in nyc is outperformed in latency by node in Germany
    - Download speed: node in nyc is outperformed in bandwidth by Cloudflare worker node (both raw bandwidth and normalized) and almost outperformed by node in Tokyo
    - Image Latency: still at the top
    
    I have observed that for media bandwidth is the best one by far in us-east and by little on us-west, and the best one in image download. Hence **I believe that we could change the node maybe to one more central to the us region**
    
- Retiring node in Mumbai, the report suggest that
    - Download speed: node in Mumbai is outperformed by the Tokyo node for South & East Asia
    - Video Latency: node in Mumbai outperformed by Singapore Node
    - Image Latency: outperformed by Singapore node for South & South-East Asia
    
    I have found however that for:
    
    - Image Latency: the node is still on top of every other node for South & South East, offering very good performance in South asia and Ok-ish performance in South-East asia
    - Download speed: it’s the best in South Asia and the Singapore node offer still good (> 50 Mbps) bandwidth in the area. The conclusion here is that even if the ping tools shows different results (performance-wise) from the report, **it can theoretically be retired** given that the Singapore node will cover the area well, however it must sustain the high traffic coming from our currently most trafficked region
- Retire St. Petersburg node, the report suggest that
    - Video Latency, Download speed, Image Latency: outperformed by node in Germany for both Europe and West Asia (especially considering the bandwidth performance offered by the Cloudflare worker)
    
    This is consistent with what the ping tool shows, hence **I agree that this node should be retired**
    
- Retire Node in Ukraine, the report suggests that:
    - Image Latency, Download speed (raw and normalised) & Video Latency : Outperformed by Germany node
    
    Ping tools confirms that the node is outperformed when downloading images, but not for video bandwidth for eu-central area, download speed offered by the Germany node is more than enough (> 50 Mbps) in both eu-central and eu-west. So this **theoretically could be also removed**
    

### Further consideration

- removing both nodes in St. Petersburg and Kyiv, will not undermine coverage for Finland / Russia, as both user and ping tools tests suggests better latency and download speed is provided by the Germany node for Europe (and West Asia)
- Although the node in the Netherlands is not the dominant node for the Europe (west + central) in all metrics it’s still needed for redundancy

## Adding nodes

I agree that one node should be added in South America given that both the report and the ping tools shows poor performance on that region and also South America is #2 by traffic currently. And I also believe that this should be a priority

# Plan

- **Add one node in South America**: this is our second region by traffic and currently we don’t have any node there
- **Change node and possibly location for the Node in the North America** region: the current node performance could be better and also there’s noticeable difference in between east/west us regions in terms of download speed
- **Retire nodes in Ukraine, St Petersburg, Mumba**i: As suggested in both reports each of this node is outperformed by a counterpart in the same geographic region. Furthermore we have at least 2 nodes in both Europe and Asian for redundancy purposes.

### Consequences

- budget reduction by around 275 USDT per month for next term (term 26)
- Better coverage for South America region
- Possibly better coverage for North America region
- Potentially higher load on the Singapore node