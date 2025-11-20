# Storage Group Operational Guide

|  | Detail | Failure will result | Exception |
| --- | --- | --- | --- |
| Setup Requirement |  |  |  |
| All storage node are required to run/configure | - Run a local validator
- Run a local Query node
- Run Storage node 
- Configure Storage node for Elastic search
- Storage node Metadata in format: All storage nodes are required to configure metadata as per the guide.
- Run Prometheus providing host, storage node and docker metrics | **Remove all Bags
Rewards reduced by %100** |  |
| All storage node are required to provide access to | - QN GraphQL URL 
- Storage node URL 
- Prometheus URL | **Remove all Bags
Rewards reduced by %100** |  |
|  |  |  |  |
| Node performance |  |  |  |
| Keep a disk usage space less than 80% | All storage nodes are required to Keep a disk usage space less than 80% | **Disable new bags
Rewards reduced by %75** |  |
| Up time | All storage nodes are required to monthly up time %99 | **Rewards reduced by %50 for the next council** | exclude down time arranged with the lead in advance. |
| Down time |  | **1 hr : Disable new bags
3 hrs : Remove all Bags
24 hrs: Disable rewards till the node is back in service and verified
120 hrs: Evict worker** | exclude down time arranged with the lead in advance |
| Node not accepting upload |  | **1 hr : Disable new bags
3 hrs: Remove all Bags
24 hrs: Disable rewards till the node is back in service and verified
120 hrs: Evict worker** | exclude down time arranged with the lead in advance |
|  |  |  |  |
| Communication |  |  |  |
| All workers are required to respond to queries within 24 hrs | - Urgent: (12 hrs) bug fix, server issue, system issue
- Medium priority: (36 hrs) work related queries.
- Low priority:(48 hrs) none work related queries | **Rewards reduced by %10 every 12 hours** |  |
|  |  |  |  |
| Council |  |  |  |
| Comply to new requirement by the council | All storage nodes are required to comply to any requirement by the council within 7 days. | **Rewards reduced by %100** |  |