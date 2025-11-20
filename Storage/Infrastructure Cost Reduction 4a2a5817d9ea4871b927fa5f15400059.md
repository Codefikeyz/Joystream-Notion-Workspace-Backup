# Infrastructure Cost Reduction

## Objective:

Optimize Joystream infrastructure to run a slim and cost effective operation while minimizing risk. 

### Actions

| Action  | Description  | Risk | Dependency  | Status  | Saving Monthly | ETA | Comments  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Reduce Storage Operators from 12 to 8  | Currently there is 80TB in the system, with each operator at a capacity less that %55 the DAO can afford to run with 8 operators | Put pressure on the capacity of the remaining operator which can trigger the next levels with upgrades. With most operators run at average 80TB total capacity now (including not unused), this can be a difficult upgrade.  | NA | Done | $2200 | NA  |  |
| Collapse Distribution operators into storage operators   | Utilize the storage server to run both distribution and storage where it is feasible | - A server outage takes out multiple functionality.
- Server resources (Bandwidth, CPU and RAM) can become and issue. 
-Can reduce the DWG flexibility  | Distribution group  | In progress  | $500 | 2 terms  | This have the added advantage of making server operators more profitable 

[https://pioneerapp.xyz/#/forum/thread/856](https://pioneerapp.xyz/#/forum/thread/856) |
| Encourage Storage and distribution to run validators | Each storage and distribution operator already run a joys stream node, all that is needed is to stake to it to make it a validator.  | - A server outage takes out multiple functionality.
  | NA | Under consideration  | NA | NA | This have the added advantage of making server operators more profitable  |
| Reduce replication needed storage capacity by reducing replication to 2 | Reduce the current replication level to 2, which half the needed storage capacity and operators. For this a backup feature to be developed. | - Operators collusion
- Rouge Infrastructure lead
- Data loss
- Data not available for sometime i.e. 24H.
- Add a level of centralization depending on how the backup is implemented. 
- Adding complexity
 | Build group  | Under consideration | $2200 | ?? | The proposal ([https://pioneerapp.xyz/#/forum/thread/811?post=6152](https://pioneerapp.xyz/#/forum/thread/811?post=6152)) is to develop a AWS deep freeze feature that makes data loss recoverable, this a DAO can afford low replication.

Personally, do not recommend it as   |