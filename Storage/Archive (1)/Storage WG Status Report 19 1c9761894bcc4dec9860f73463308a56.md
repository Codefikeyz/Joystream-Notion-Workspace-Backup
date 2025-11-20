# Storage WG Status Report 19

Summary report for the Term: 19

Dates: 10 August 2022 - 18 August 2022

Start block: 2001600 0x481eeee3c1114b0b93416fee47920be70e99d45b56a5d6904b540608747fc73a

End block: 2116800 0xe4a788b0d10000fd5ca3447612e727f1cdbfe5fe3a272baf49d0107e1075881f

WG Lead: 0x2bc

WG Deputy Lead: yasir

## 1. 💵 Accounting

**Budget at the start of the term: 0.5171710** MtJOY 
**Budget refilled during the term: 13.0** MtJOY
**Discretionary spendings**: 0.0 MtJOY
**Lead rewards: 2.336040** MtJOY
**Worker rewards: 9.993060** MtJOY
**Budget at the end of the term:** **2.5579** MtJOY

## Group Changes

## 2. Group Changes

### Hires

- no

### Slashes

- no

### Firings

- no

## 3. Timesheet

This is based on self-reporting info

|  |  **Hours of Work** |
| --- | --- |
| Worker ID 0 - Lead (0x2bc) | 10 |
| Worker ID 1 (joystreamstats) |  |
| Worker ID 2 (alexznet) | 1 |
| Worker ID 3 (maxlevush) |  |
| Worker ID 4 (l1dev) |  |
| Worker ID 5 (GodsHunter) | 1 |
| Worker ID 7 - Deputy Lead (yyagi) | 1 |
| Worker ID 8 (mmx1916) |  |
| Worker ID 9 (Craci_BwareLabs) | 1 |
| Worker ID 10 (razumv) | 1 |
| Worker ID 11 (sieemma) | 3 |
| Worker ID 13 (plycho)  |  |
| Worker ID 14 (abramaria_) | 2 |
| Worker ID 15 (kalpacki) | 1 |

**Lead Extra Hours: no**

## 4. Bounties for newcomers

- no new bounties (we are not looking for newcomers in the Storage WG!)

## 5. Notion Board Changes

- No changes

## 6. **List of completed tasks**

- Developed tasks required by the new Bonus system
- Keep educating the Deputy Lead about the Lead tasks
- Carthage release testing        [ongoing work]
- Improved STORAGE_SCORE  [one more worker set up his “extra” attribute in metadata]

## 7. **Ideas to improve your Working Group**

the same as usual:

- Remove worker opportunities score
- Feedback on the scores is extremely helpful. Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.

Not sure that i fully understand these Scores

- SYSTEM_SCORE:
    - All storage nodes display their location coordinates, node storage capacity and **caching** in the metadata (what is caching?)
    - All storage that has been in the working group for more than 1 week (100,800 blocks), must maintain their own query node, and **share the public url** in the metadata (where should it be shared?)

## 8. **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project

# SHORT REPORT

- How many storage buckets were created.

see BUCKETS CREATED section

- How many storage buckets were deleted.

see BUCKETS DELETED section

- What was the capacity and utilization of each storage bucket at the beginning and end of the term (number and size of data objects).

see BUCKETS Info table

- How many bags were created.

see BAGS section

- How many bags were deleted.

see BAGS section

- What data objects were permanently lost, and if any, why.

see Lost Objects - GraphQL section

- How many data objects were (attempted) uploaded, andwhat was their total size,what was the size distribution.

see Objects Info during this Council Period section

- List of failed data upload upload attempts on chain, and if possible to find out - why.If this is not done, the `UPLOAD_SCORE` will assume all uploads failed independently, and that the group is at fault.

see Lost Objects - GraphQL section

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:data objects, number and size;amount of bags;(average) number and size of data objects in a bag

see Charts 

- What is the current running costs for the system, and a breakdown of said costs.

see Current costs  section

- How much bandwidth did the individual nodes consume during the period.

see Bandwidth Usage  section

- What, if anything, is the storage group doing the monitor the health of the system.

see see Monitoring  section

- A list of all `storage` transactions (not `storageProviderWorkingGroup`) made by the lead, and the purpose behind them.

see Transactions section

- An overview of which nodes that running with `--elasticSearchEndpoint`, what log level they are using, and how this information is used.

see Elastic Search Logging section

# FULL REPORT

# Rewards

Total Rewards: 12329100

[Rewards](Storage%20WG%20Status%20Report%2019/Rewards%20d83fab4b7ed84f4eadb61679b950b269.csv)

# BUCKETS Info

[BUCKETS Info](Storage%20WG%20Status%20Report%2019/BUCKETS%20Info%2099f60988915d496d87ce74cbc1f026a0.csv)

## BUCKETS CREATED

Bucket Created: 0

## BUCKETS DELETED

Bucket Deleted: 0

## BAGS

Bags Created: 7

Bags Deleted: 0

# Lost Objects - GraphQL

Total Objects: 81

Total Lost Objects: 1

Percentage Lost Objects: %1.23

[Lost Objects](Storage%20WG%20Status%20Report%2019/Lost%20Objects%202d8e12c4866e4144aa2f22fb4fe5ded2.csv)

# Objects Info during this Council Period

Total Objects Size: 81

Total Objects Size: 6372647407

## Objects Size Distribution

[Objects Size Distribution](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%20e29c024d1f68493e9869d13d9f122dec.csv)

[Objects Size Distribution](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%205f5215cea3f34a8db02a4079065d4d1c.csv)

## Objects Size Distribution Per Bag

[Objects Size Distribution Per Bag](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%20Per%20Bag%204012588e20564dbaa3d22466f0a5cc34.csv)

# Total object Info (Over all time)

Total Objects: 15578

Total Objects Size: 949944604094 bytes

Total Number of Bags in use: 635 bytes

Grand Total Number of Bags: 674 bytes

## Objects Size Distribution

[Objects Size Distribution\](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%20634fc72ae989469c83b764d1c0c3ea63.csv)

[Objects Size Distribution](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%200f1006f2fc43451c88d3a9aee0eab1ac.csv)

## **Objects Size Distribution Per Bag**

[Objects Size Distribution Per Bag](Storage%20WG%20Status%20Report%2019/Objects%20Size%20Distribution%20Per%20Bag%20a11a6810039d458183e1f598fd1ffbae.csv)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2019/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2019/Untitled%201.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2019/Untitled%202.png)

# Elastic Search Logging

Connected nodes:

- MMX
- Yasir
- Maxlevush
- kalpakci
- sieemma
- 0x2bc
- joyrq
- Craci_BwareLabs

Log level: 

- Default: debug

# Bandwidth Usage

See here for traffic Analysis : 

- [https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Flows-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Flows-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))
- [https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Dashboard-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Dashboard-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))

## Monitoring

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage nodes [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload 
    (3) On a daily basis: monitor status of the storage nodes
    
     [https://kibana.joystreamstats.live/app/dashboards](https://kibana.joystreamstats.live/app/dashboards)
    
    [https://kibana.joystreamstats.live/app/dashboards#/view/Metricbeat-system-overview-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Metricbeat-system-overview-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))
    
    </aside>
    

## Transactions

- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.

Added all bags to worker ID (bucketID)=14 to get one more backup server

for i in $(seq 2000 2669) ; do
yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 14 -p 7WuZaFA419bO1
done

[Current costs ](Storage%20WG%20Status%20Report%2019/Current%20costs%20d19017bc9d6642d1abe025e80b3c9bf1.csv)