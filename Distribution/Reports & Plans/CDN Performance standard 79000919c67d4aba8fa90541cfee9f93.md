# CDN Performance standard

Date last reviewed: 2024.03.25

## Document scope

Standardise and provide benchmarking procedure that can be easily repeated and provide relevant CDN metrics

### Glossary:

- DN = distributor node
- SN = storage node
- monitoring server = server deployed with purpose to collect CDN metrics and display them under a grafana and kibana dashboards
- ping location = location where script for data monitoring used in our Ping tool will be deployed
- ping tool = our stack comprising of script deployment and `distribution dwg` dashboard used in decision making when reviewing our geographic coverage
- ✅ = satisfied

### Request structure

Scenario: client send a GET request to a DN for an image, here’s the sequence of steps 

1. **Socket Initialization:** This is the time taken to prepare the request on the client side before it is sent. I will denote this time with 
2. **DNS Lookup:** The time spent in resolving the domain name of the URL into an IP address.
3. **TCP Handshake:** This represents the time taken to establish a TCP connection between the client and the server.
4. **SSL Handshake:** If the connection is over HTTPS, this is the time taken for the SSL/TLS handshake, which establishes a secure connection.
5. **Transfer Start:** This is the point at which the first byte of the response is received by the client. It is effectively the end point for calculating TTFB.
6. **Download**: This is the time taken to download whatever asset the client has requested starting from when the first byte has been received by the client

Detail relevant metrics for Distributor nodes in our CDN:

<aside>
💡 **Ping RTT**: this values is obtained by executing a `ping DNS_NAME` on the command line and measure the Round Trip Time (RTT) taken by the request with minimum data to travel from the client to the DN to and back. This measures latency in the most basic sense, trying to reduce impact of points 5-6 in the measurement

</aside>

An easy way to manually issue ping tests is to use the following service: [https://www.cdnperf.com/tools/cdn-latency-benchmark/](https://www.cdnperf.com/tools/cdn-latency-benchmark/)

<aside>
💡 **TTFB**: Time to First Byte is computed as the sum of socket init + dns lookup + tcp handshake + ssl handshake + transfer start. This effectively measures the time in between the request is sent and the first byte of data is received. It strongly impacts page and video loading  [*(This is also crucial for Atlas in deciding which node to fetch the video from when streaming)*](https://github.com/orgs/Joystream/projects/64?pane=issue&itemId=49110656)

</aside>

Our “ping tool” measures this for both image and video assets however it is limited by the location deployed, a manual alternative is provided by this [https://speedvitals.com/ttfb-test](https://speedvitals.com/ttfb-test). Also [Amazon CDN](https://aws.amazon.com/blogs/networking-and-content-delivery/measuring-cloudfront-performance/) recommends using last byte latency (LBL) or response time over first byte latency (FBL), as most applications will not be able to serve content until the last byte is delivered.

<aside>
💡 **Bandwidth**: this is defined as the size in Mbits of the asset received divided by the Download time (point 6) and it measures how much data can the server send in the given time. It strongly impact the video streaming experience

</aside>

Our “ping tool” also measures the bandwidth 

<aside>
💡 Cache hit ratio: How many requests the DN is able to serve by fetching an asset on its local volume divided the number of request sent. This is trying to measure how many time the DN is forced to ask a SN for a missing asset

</aside>

Currently our “ping tool” is missing this metrics, but I believe it can be produce easily starting from the Argus node and piped into elastic search

## Measuring techniques

- Using synthetic data: approach achieved by the ping tool deploying script instances on various geographic location and collect data on the monitoring server
- Using RUM (real user monitoring): Gleev sends relevant metrics directly to monitoring server. ~~This is in the pipeline for Q1-2024.~~ Achieved

[Amazon CDN](https://aws.amazon.com/blogs/networking-and-content-delivery/measuring-cloudfront-performance/) suggest RUM over Synthetic, but for the time being I think it’s worth enhancing the coverage of our ping tool

# Synthetic measuring

RUM data will take care of giving us the best geographic coverage we need, until then we have to focus on synthetic data and our ping tool. In proposing the configuration below I have followed the rules below

### A few rules of thumb when choosing ping locations

1. There should not be any DN deployed in (or close by) a ping location. For example we had a node in Mumbai which was also one ping location, thus ttfb values were too optimistic and provided no much aid in decision making
2. Ping location should be uniformly dispersed across the whole geographic area we want to cover and should be reflective of our current traffic (that is we very few traffic coming from Oceania, so I don’t see any necessity of having a ping location over there)
3. Try to leverage Google Cloud Provider locations [https://cloud.google.com/compute/docs/regions-zones](https://cloud.google.com/compute/docs/regions-zones) as the current monitoring operator has a GCP subscription. Beyond those location provided by GCP there is also one location provided by OVH (Singapore)

### North America

- N. Virginia, GCP: `us-east-4` ✅ (currently we have `us-east-1` South Carolina)
- Oregon, GCP: `us-west-1`

### South America

- Santiago, GCP: `southamerica-west-1`
- Sao Paolo, GCP: `southamerica-east-1` : we have to be careful here as now we have a DN in Sao Paolo

<aside>
💡 For most cloud providers location there are only these two locations in South America, for our ping locations setup I will suggest moving the ping location from Sao Paolo to Santiago.

</aside>

### Europe

- Warsaw, GCP: `europe-central-2` ✅
- Madrid, CGP: `europe-southwest-1` ✅ (currently we have `europe-west-2` London)

### Middle East

- Tel Aviv, GCP: `me-west1-1`

### South Asia

- Delhi, GCP: `asia-south-2` or Mumbai, GCP: `asia-south-1` ✅
- Jakarta, GCP: `asia-southeast-2` ✅

### NorthEast Asia

- Seoul, GCP: `asia-north-east-3`  (currently we have `asia-northeast-1` Tokyo and we also have a DN in Tokyo). I recommend changing the ping location

# Target values

### Collecting data from ping locations

Once we have our synthetic data set up we could aim for the following target metrics:

1. We pick a time window of 15 days with the hope that the sample distribution is stationary for that period. And also we fix two `assetId`s one for an image type and another for the video type. This `assetId` s will be always the same when sampling (t***his also implies that we are using cached assets***)
2. Established the time frame we collect `bandwidth` and `ttfb` sample values for each of the active DNs from each deployment.
3. For each ping location `i` and for each DN location `j` we 
    - sample `median_ttfb[i][j]` as the median value over the ttfb samples collected for that ping location against DN `j` and then we defined the `best_median_ttfb[i]` as the lowest ttfb value across all DNs.
    - compute `median_bandwidth[i][j]` as  the median value over the bandwidth samples collected for that ping location against DN location `j` and then we defined the `best_median_bandwidth[i]` as the highest bandwidth across all DN locations.
    
    <aside>
    💡 **Remark**: If we have a ping location `i = Seoul` we should expect that the location `j*` for which min ttfb and max bandwidth to be achived should be `j* = Tokyo` (as we have a DN in Tokyo), if it not so we should consider retiring that node (as we did in the previous benchmark)
    
    </aside>
    
4. At the end of our process the **for each** deployment location `i` we have to satisfy
    - `best_median_bandwidth[i]` > 20 Mbps (that is there are no location measuring a median bandwidth value less than 20 Mbps). This value should be sufficient for smooth 1080p video streaming
    - `best_median_ttfb[i]` < 350 ms (that is there are no location measuring a median ttfb value more than 350 ms). This value is considered slightly better than average for page loading (ref: [https://speedvitals.com/ttfb-test](https://speedvitals.com/ttfb-test))

### Collecting Cache hit samples

1. Create a PR for piping cache hit ratio into the Elastic search logs, and as previously we fix a time window of 15 days
2. For each DN location `j` we sample compute the `average_cache_hit_ratio[j]` over the time samples for window considered
3. As target we want to satisfy that for every DN location `j` `average_cache_hit_ratio[j] > 30%`

## Comments on the target values chosen

I have inquired chatgpt for the target bandwidth value as it recommends 

> **High-Quality 1080p:** For higher quality, such as videos with a higher bit rate or using better compression methods like H.265 (which offers similar quality at a lower bit rate), you might need around 8-10 Mbps
> 

According to our synthetic data measurement this requirement is already met by our current CDN configuration 

I have used the [https://speedvitals.com/ttfb-test](https://speedvitals.com/ttfb-test) and chatgpt recommends the same range of values. Obtaining this values will be probably a challenge especially in the South America and Africa region as most cloud provider services have just nodes in Sao Paolo, Santiago, Johannesburg for these two macro regions and also the internet infrastructure is not as developed as the one in Europe or North America (where this target values can be easily met)

**Cache hit ratio**: chatgpt suggests that for dynamic content a value in between 30%-60% would be considered good

# RUM measuring

Using Real user monitoring data

The document discusses various factors that can influence the discrepancy between average latency values for Central Europe and the significantly lower latency on certain specific connections.

### Factors that can affect measurement

1. **Internet Service Provider (ISP) Performance**: The efficiency of your ISP's routing, its bandwidth capacity, or the level of congestion can result in lower latency for users connected through this ISP.
2. **Physical Proximity to the Server**: The physical distance between the user and the server greatly influences latency. Users geographically closer to the server hosting the content will likely experience lower latency.
3. **Network Infrastructure**: The quality of the network infrastructure, including number of hops and presence of high-speed links, can greatly affect latency. A more direct network path or higher quality infrastructure will result in lower latency.
4. **Local Network Conditions**: The condition of your local network, such as absence of heavy internal traffic or quality of networking hardware, can contribute to lower latency.
5. **Content Delivery Networks (CDNs)**: CDNs can significantly reduce latency by caching content closer to the end-user. If the services you are accessing utilize CDNs, your location might be better served by a CDN node that is closer or less congested.
6. **Time of Access**: Network congestion varies throughout the day. Accessing services during off-peak hours when fewer users are online might result in lower latency.
7. **Adaptive Technologies**: Some networks use adaptive technologies to optimize the route or the protocol based on real-time conditions. These technologies might optimize your connection more effectively.
8. **Measurement Methodologies**: If the methodology for collecting Real User Monitoring (RUM) data differs from how you measure your latency, this might result in apparent discrepancies.

Some techniques to reduce the influence of the above factor

To obtain more accurate and controlled measurements of your service's performance, independent of end-user connection variability, consider employing the following approaches:

1. **✅ Synthetic Monitoring**: This method uses bots or scripts to simulate user interactions from various locations and on different devices. It allows for control over variables such as network conditions, device type, and geographic location, thereby isolating the performance of your application or website from users' internet connections.
2. **Server-side Metrics**: Focusing on metrics measured on the server-side, like server response time, database query performance, and backend processing times, provides insight into your infrastructure's performance. These metrics reflect the performance of your server and backend systems before the data starts its journey to the user.
3. **Controlled Load Testing**: This approach involves generating traffic to your site using test scripts or tools simulating a predetermined number of users or requests per second. By controlling the test conditions, you can better understand how your system performs under various loads, independent of real user behavior.
4. **Aggregated Data Analysis**: When using Real User Monitoring (RUM) data, applying advanced statistical analysis and filtering techniques can help minimize the impact of outliers or extreme values. Aggregating data into percentiles (e.g., the 90th percentile) rather than averages can provide a more accurate picture of the user experience for the majority of your users, while filtering out extreme cases.

### Goals and observations

- We're currently dividing TTFB and bandwidth for images and videos (media) in the synthetic data. Should we apply the same approach to RUM data?
- We're using the median as an aggregation statistic over a specific timestamp for the following reasons:
    - **Resilience to Outliers**: The median is less affected by extremes or outliers in data.
    - **Representative of Typical User Experience**: As the middle value, the median more accurately reflects the typical user's experience.
    - **Ease of Interpretation**: It indicates that half of your users experience better performance than this value.
    - **Temporal Trends**: Over time, the median can highlight trends without the noise from outliers.
- Another possible statistic is the 90% quartile.
- Elasticsearch records don't contain a specific field for cloud regions (e.g., us-central, eu-central, etc.), but they do have a country field (US, PL, IN, etc.). As we can't display all countries, and some, like Oceania, have very few users, we need to identify the top countries with the most active users.

Based on the above I propose the following measurement procedure:

### Measurement for RUM data

1. RUM Data is collected into the Elasticsearch cluster.
2. Define `topCountries` as the top 10 countries, aggregated by a unique count of records over a fixed term length of 28 days. Alternatively, these could be the 20% (or fewer) of countries that produce 80% (or more) of the unique records.
3. From this, we can measure median TTFB and Bandwidth values, and potentially the 90% percentile. A better approach might be to have a dedicated dashboard for both TTFB and Bandwidth, displaying box plots for each of the `topCountries`. **For OKR assessment I suggest we stick to the median value as a summary statistic**
4. As an OKR goal, it would be acceptable to have a Bandwidth and TTFB Latency value for each country. This is because network performance can vary significantly between countries, such as Germany (a highly developed country) and Bangladesh (a developing country). I suggest using reference values for each country from this [website](https://www.speedtest.net/global-index/germany?fixed#market-analysis), where:
    - Multiserver latency is our reference latency .
    - Download speed is our bandwidth.
    - They provide values for mobile and fixed connections. We could use these as a reference and consider distinguishing between mobile and fixed connections in our logs if possible.
    - We should look at the market research reports for each country if available for which the multiserver latency is available is provided, for OKR assessment we should use the worst ISP value. If market research page is not provided we should use the one from the nearest geographical country. (see picture for reference)
5. In June 2024, we will compare values for the `topCountries` with those from the SpeedTest website. If our median Bandwidth and TTFB values are above the country average, then we have reached our OKR. This would suggest: "Our coverage of that country in terms of Bandwidth and Latency is above average in terms of the average resident user experience".

## When to add an extra operator

Not relevant to the OKR strictly speaking, but the above configuration suggests, In this sense it makes sense to add an operator in a particular region when the following conditions are satisfied:

1. region (eu-central, us-central etc…) contains a country that it is in the `topCountries` for at least the past 2 terms (that is select the last 56 days time window from the Kibana dashboard)
2. None of the current distribution nodes can provide an actual value for Bandwidth and Latency that it is less than 10% of the target value