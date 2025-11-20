# Term 12

### Term 12 Plan (02.06.23 - 17.06.23)

### 1. Current WG composition:

- [@klaudiusz](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=2233) - Lead, worker
- [@0x2bc](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=2098) - worker
- [@adovrn](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=2502) - worker
- [@sieemma](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=458) - worker
- [@goksel](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=3655) - worker
- [@Craci_BwareLabs](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=3886) - worker
- [@lkskrn](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=644) - worker
- [@Deathix](notion://www.notion.so/joystream/Distributor-node-space-optimization-9995a91e58384e4fae525f12c65b502d?p=b4462f943b474a14b02054d58f6506e5&showMoveTo=true#mention?member-id=4236) - worker

**Comment:** Following my analysis done last term ([https://joystream.notion.site/Traffic-analysis-2023-05-27-3f5fb9b19e1241c9a28b68bf23499dc3?pvs=4](../Traffic%20analysis%202023-05-27%203f5fb9b19e1241c9a28b68bf23499dc3.md)), I’m not planning to hire any regular workers until some specific need arises. I may consider hiring someone to help with monitoring DWG operations in next terms.

### 2. Planned WG budget:

**Regular workers salaries:** 8 * 11,660 JOY = 93,280 JOY

**Monitoring worker salary:** 3,000 JOY

**Lead salary:** 41,040 JOY

**Total spending:** 137,320 JOY

**Comment:** Following council support for SWG proposal ([https://pioneerapp.xyz/#/proposals/preview/342](https://pioneerapp.xyz/#/proposals/preview/342)), this term I’ve planned to double regular and monitoring (not lead) worker salaries. Figures above already include this change. Like stated previously, this increase will make salaries more competitive and decrease the gap between regular workers and lead and council.

### 3. WG OKRs:

| **No.** | **Objectives** | **Status** | **Key Results** | **Term initiatives** |
| --- | --- | --- | --- | --- |
| **1** | **Introduce availability monitoring** | *In progress* | 1) Develop additional monitoring for total node availability, including disabled buckets | 1.1) Continue writing a small tool to ping all the operators and collect statistics from QN
1.2) Deploy the monitoring tool |
| **2** | **Improve logs collection setup** | *In progress* | 1) Grant SWG access to Elasticsearch
2) Implement a more resilient Elasticsearch setup | 1.1) Add user accounts for SWG workers and lead with correct permissions
2.1) Migrate Elasticsearch from a single node to a 2-node cluster |
| **3** | **Introduce video loading and bandwidth monitoring** | *New* | 1) Implement basic bandwidth monitoring for images
2) Enhance request tracing
3) Introduce video bandwidth monitoring
4) Collect and analyze data over a few days to instruct further initiatives | 1.1) Develop changes to the monitoring setup to enable image downloading and collect statistics
1.2) Include bandwidth statistics in the monitoring dashboard
2.1) Review Argus changes: [https://github.com/Joystream/joystream/pull/4779](https://github.com/Joystream/joystream/pull/4779) |

### Term 12 Report (02.06.23 - 17.06.23)

### 1. Current WG composition:

- [@klaudiusz](https://pioneerapp.xyz/#members) - Lead, worker
- [@0x2bc](https://pioneerapp.xyz/#members) - worker
- [@adovrn](https://pioneerapp.xyz/#members) - worker
- [@sieemma](https://pioneerapp.xyz/#members) - worker
- [@goksel](https://pioneerapp.xyz/#members) - worker
- [@Craci_BwareLabs](https://pioneerapp.xyz/#members) - worker
- [@lkskrn](https://pioneerapp.xyz/#members) - worker
- [@Deathix](https://pioneerapp.xyz/#members) - worker

No changes in WG's composition at the moment, however 2 openings were created and the group is looking to expand:

- Infrastructure / Monitoring Engineer - [https://pioneerapp.xyz/#/working-groups/openings/distribution-10](https://pioneerapp.xyz/#/working-groups/openings/distribution-10)
- DWG Deputy - [https://pioneerapp.xyz/#/working-groups/openings/distribution-11](https://pioneerapp.xyz/#/working-groups/openings/distribution-11)

### 2. WG budget spending:

**Planned spending:** 137,320 JOY

**Starting budget:** 20,324.25 JOY

**End budget:** 82,747.75 JOY

**Budget refill:** 200,000 JOY

**Total spending:** 20,324.25 JOY - 82,747.75 JOY +  200,000 JOY = 137,576.5 JOY

**Comment:** Total spending is a bit higher than planned since lead salary in the plan assumes 15 days, while the term is actually slightly longer, hence few more JOYs were paid.

### 3. OKRs progress:

*Reference: [https://pioneerapp.xyz/#/forum/thread/85?post=3853](https://pioneerapp.xyz/#/forum/thread/85?post=3853)*

- OKR 1 (Introduce availability monitoring):
Status: Done
Comment: New availability tool was developed and deployed: [https://github.com/kdembler/operators-availability](https://github.com/kdembler/operators-availability) This pings all the operators every 5 minutes and checks things like QN sync status, that they are connected to the correct chain, etc.
- OKR 2 (Improve logs collection setup):
Status: In progress
Comment:
Initiative 1.1) (support for SWG) was completed.
Initiative 2.1) (migrating to a 2-node cluster) is in progress.
- OKR 3 (Introduce video loading and bandwidth monitoring):
Status: In progress
Comment:
Initiative 1.1) (image bandwidth monitoring) is still in progress and not yet deployed.
Initiative 2.1) (Argus tracing PR review) is ongoing - review of both code and functionality was done, all the necessary infra was set up and feedback was sent to the PR implementer. Currently waiting for fixes and will deploy this across WG.

Comment: Progress this term wasn’t fantastic, that’s mostly because of lead’s low availability (planned vacation + personal life complications). We expect to catch up during the next term. To alleviate lead being a bottleneck, 2 openings were created for WG (as mentioned in WG composition section), so the workload may be better split going forward.

### 4. DWG stats

1. All nodes average latency in their respective region was <250ms.
2. DWG nodes served over 7000 unique users.
    1. Russia (16%), Indonesia (15.6%), Ukraine (10.7%) and US (9.6%) are leaders of unique visitors
3. DWG nodes handled over 1.2M asset requests.
    1. Russia (20.5%) still leads in the number of requests, followed by Ukraine (12.3%) and Turkey (10%).