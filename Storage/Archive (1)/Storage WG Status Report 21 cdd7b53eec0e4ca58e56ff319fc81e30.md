# Storage WG Status Report 21

Summary report for the Term: 21

Dates: 25 August 2022 - 2 September 2022

Start block: 2217600 0xcf5f28c197f7ab8e98624279fcc6eb8529d62a02bbe0bca559a78ae4ea430d03

End block: 2332800 0x2557284dd95b413b9a81486bb013bbd2242726e067e343f04a05667a8584ad98

WG Lead: 0x2bc

WG Deputy Lead: yasir

## 1. 💵 Accounting

**Budget at the start of the term: 2.9686** MtJOY
**Budget refilled during the term: 10.0** MtJOY
**Discretionary spendings**: 0.0 MtJOY
**Lead rewards: 2.049222** MtJOY
**Worker rewards: 8.973382** MtJOY
**Budget at the end of the term:** **1.946** MtJOY

## Group Changes

## 2. Group Changes

### Hires

[Hires ](Storage%20WG%20Status%20Report%2021/Hires%202f1e380df0d0453ab6223eb891202cb3.csv)

### Slashes

- no

### Firings

[Firings](Storage%20WG%20Status%20Report%2021/Firings%201851abb563c748dcba30354f525bd709.csv)

## 3. Timesheet

This is based on self-reporting info

|  |  **Hours of Work** |  |
| --- | --- | --- |
| Worker ID 1 (joystreamstats) |  |  |
| Worker ID 2 (alexznet) | 1 |  |
| Worker ID 3 (maxlevush) | 1 |  |
| Worker ID 4 (l1dev) |  |  |
| Worker ID 5 (GodsHunter) | 1 |  |
| Worker ID 8 (mmx1916) | 1 |  |
| Worker ID 9 (Craci_BwareLabs) |  |  |
| Worker ID 10 (razumv) |  |  |
| Worker ID 11 (sieemma) | 2 |  |
| Worker ID 13 (plycho)  |  |  |
| Worker ID 14 (abramaria_) | 2 |  |
| Worker ID 15 (kalpacki) | 1 |  |
| Worker ID 16 - Lead (yyagi) | 15 |  |
| Worker ID 18 - Deputy Lead(0x2bc) | 4 |  |

**Lead Extra Hours: no**

## 4. Bounties for newcomers

- no new bounties (we are not looking for newcomers in the Storage WG!)

## 5. Notion Board Changes

- No changes

## 6. **List of completed tasks**

- New lead is active
- New deputy is active
- Developed tasks required by the new Bonus system
- Maintained STORAGE_SCORE
- Carthage release testing is in progress

## 7. **Ideas to improve your Working Group**

the same as usual:

- Feedback on the scores is extremely helpful. Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.
- Evicting a user should remove the bucket and bags associated, or force the admin to do the clean up before proceeding.

## 8. **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project
- Think of reducing documentation and automate data reporting. Most requested data in this report can be automated.

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

Total Rewards: 11022604

[Untitled](Storage%20WG%20Status%20Report%2021/Untitled%20d65a23fc6f9a4dbfa9f6564afa29b37c.csv)

# BUCKETS Info

# BUCKETS Info

[Untitled](Storage%20WG%20Status%20Report%2021/Untitled%20f9ee602ba3ff4dbabee765cdf8738ab3.csv)

## BUCKETS CREATED

Bucket Created: 2

[BUCKETS CREATED](Storage%20WG%20Status%20Report%2021/BUCKETS%20CREATED%20bd61a1d598644160b19704dd5a76b27b.csv)

## BUCKETS DELETED

Bucket Deleted: 0

## BAGS

Bags Created: 12

Bags Deleted: 0

# Lost Objects - GraphQL

Total Objects: 123

Total Lost Objects: 31

Percentage Lost Objects: %25.203252032520325

[Lost Objects](Storage%20WG%20Status%20Report%2021/Lost%20Objects%206c497267f04d4df983051768bab19c40.csv)

# Objects Info during this Council Period

Total Objects Size: 123

Total Objects Size: 5238548334 bytes

## Objects Size Distribution

[Objects Size Distribution](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%2075a17657c17d44ff8fa40353e7b5eb92.csv)

[Objects Size Distribution](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%2076845314c8bc4a27ba0e6a9329622a0e.csv)

## Objects Size Distribution Per Bag

[Objects Size Distribution Per Bag](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%20Per%20Bag%20aa5e56486f3a4acd9479575525bfd95c.csv)

# Total object Info (Over all time)

Total Objects: 15769

Total Objects Size: 959895072627 bytes

Total Number of Bags in use: 651 bytes

Grand Total Number of Bags: 699 bytes

## Objects Size Distribution

[Objects Size Distribution](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%208961a13b8d6f49048df3dadba6ac6705.csv)

[Objects Size Distribution](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%20ca64ff649959483696a9981e453d59e3.csv)

## **Objects Size Distribution Per Bag**

[Objects Size Distribution Per Bag](Storage%20WG%20Status%20Report%2021/Objects%20Size%20Distribution%20Per%20Bag%20316ce22e4b8b415999808421f7977c91.csv)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2021/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2021/Untitled%201.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2021/Untitled%202.png)

# Elastic Search Logging

Connected nodes:

- ALEXZNET_SP
- joyrq_SP
- sieemma_SP
- 0x2bc_SP
- abramaria_SP
- YYAGI2_SP
- 3886-Craci_BwareLabs_SP

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

Transiting from users to leader and hiring the old leader as a deputy leader

yarn joystream-cli working-groups:evictWorker 7 --group=storageProviders
yarn joystream-cli working-groups:fillOpening --openingId 22 --applicationIds 39
yarn joystream-cli working-groups:fillOpening --openingId 23 --applicationIds 40
yarn joystream-cli working-groups:cancelOpening 25
yarn joystream-cli working-groups:createOpening -g=storageProviders -i ~/joystream_working_dir/Strorage_WG_Deputy_Leader.json
yarn joystream-cli working-groups:createOpening -g=storageProviders -i ~/joystream_working_dir/Strorage_WG_Worker.json
yarn joystream-cli working-groups:evictWorker 17 --group=storageProviders
yarn storage-node leader:create-bucket -i 16 -n 20000 -s 1500000000000 -k /root/keys/storage-role-key.json -p xxxxxx
yarn storage-node leader:update-bucket-status -i 16 -s off -k /root/keys/storage-role-key.json -p xxxxxx
yarn storage-node leader:create-bucket -i 17 -n 20000 -s 1500000000000 -k /root/keys/storage-role-key.json -p xxxxxx
yarn storage-node leader:update-bucket-status -i 17 -s off -k /root/keys/storage-role-key.json -p xxxxxx

[Current costs ](Storage%20WG%20Status%20Report%2021/Current%20costs%20484f4232daf94fa88a72603da45230cc.csv)