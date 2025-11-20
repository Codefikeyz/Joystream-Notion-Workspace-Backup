# Storage SP Bounty

*Last updated: 16 May 2022*

The page contains list of Storage WG bounties and requirements for tech systems. These systems can make life easier and improve the performance of Storage WG  as a whole. 

## Table of Contents

## Bounty 1: Storage Dashboard

**Short description:** Storage Dashboard shows information about Storage WG day-to-day operations and status of the Storage system in a way that is convenient for decision making. 

**Purpose:** To help the Lead to identify potential risk events that may impact Storage System.

**Requirements:** 

![SP dashboard - requirements.png](Storage%20SP%20Bounty/SP_dashboard_-_requirements.png)

**Related info:**  

Current storage dashboard: 

[https://olympia.joystreamstats.live/storage](https://olympia.joystreamstats.live/storage)

GitHub issue: 

[https://github.com/Joystream/community-repo/issues/656#issuecomment-1105156670](https://github.com/Joystream/community-repo/issues/656#issuecomment-1105156670) 

## Bounty 2: Automated reporting system

**Short description:** Reporting system generates reports for Storage (and Distributors) work groups in a fully automated way.

**Purpose:** 

(1) ****Make the reporting process unified with Distribution WG. 

(2) Save the Lead’s time and prepare weekly  reports in an automated way

**Requirements:** 

Automated report system should generate reports including the following information:

- How many storage buckets were created.
- How many storage buckets were deleted.
- What was the capacity and utilization of each storage bucket at the beginning and end of the term (number and size of data objects).
- How many bags were created.
- How many bags were deleted.
- What data objects were permanently lost, and if any, why.
- How many data objects were (attempted) uploaded, and
    - what was their total size,
    - what was the size distribution.
- List of failed data upload upload attempts on chain, and if possible to find out - why.
    - If this is not done, the `UPLOAD_SCORE` will assume all uploads failed independently, and that the group is at fault.
- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size;
    - amount of bags;
    - (average) number and size of data objects in a bag
- What is the current running costs for the system, and a breakdown of said costs.
- How much bandwidth did the individual nodes consume during the period.
- What, if anything, is the storage group doing the monitor the health of the system.
- A list of all `storage` transactions (not `storageProviderWorkingGroup`) made by the lead, and the purpose behind them.

**Related info:**  

For reference see “real” reports:

| **#** | **Report** | Status | **Period**  |
| --- | --- | --- | --- |
| 1 | [Storage WG Status Report 1](Archive/Storage%20WG%20Status%20Report%201%2056644051c11b4182815f2d41cf6b6541.md) | Done | 28 March 2022 - 3 April 2022 |
| 2 | [Storage WG Status Report 2](Archive/Storage%20WG%20Status%20Report%202%200a63f7d37e2247dda85591fc755973d2.md) | Done  | 4 April 2022 - 10 April 2022 |
| 3 | [Storage WG Status Report 3](Archive/Storage%20WG%20Status%20Report%203%209fce0bd1781849e3b67f6da1e1344376.md) | Done | 11 April 2022 - 22 April 2022 |
| 4 | [Storage WG Status Report 4](Archive/Storage%20WG%20Status%20Report%204%20458b167a4e1c4bab885118ba9c7bffb9.md) | Done | 23 April 2022 - 29 April 2022 |

Requirements to the reports:

[https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score)  

## Bounty 3: Performance Tests

**Short description:** These tests measure some parameters of the Storage System that are important but sill are not included in the Storage WG Score.

**Purpose:**  Get an in-depth understanding of the Storage Nodes performance. Find “weak” nodes before they make any damage to the Storage System.

**Requirements:** 

Tests should numerically measure the following parameters: 

- Low latency and reliable uploading.
- Very low probability of permanent data loss
- High upload speed.
- High upload volume capacity: many simultaneous parallel uploads.
- A high upload speed to distributors.
- A low replication latency for a new data objects to all providers for the given bag.
- A low synchronization time of new storage providers.
- Basic level of denial of service resistance at the public upload API.

**Related info:**  

Requirements to the Storage OKRs and KPIs:

[https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score)  

Also see old Storage OKRs on the GitHub

## Bounty 4: Notification Bot - DONE

**Short description:** Notification Bot in Discord helps everyone in the #Storage Discord channel see important updates of the Storage WG. 

**Purpose:** For the Storage WG: being more transparent. For the Joystream community members: getting important information in a rapid way.

**Requirements:** 

Notification Bot should provide notifications on the following updates:

- salary change
- hiring
- firing
- failed uploads
- current storage size (on-demand)
- change in the group’s treasury

See examples for the 

![Untitled](Storage%20SP%20Bounty/Untitled.png)

![Untitled](Storage%20SP%20Bounty/Untitled%201.png)

![Untitled](Storage%20SP%20Bounty/Untitled%202.png)

![Untitled](Storage%20SP%20Bounty/Untitled%203.png)