# Storage WG Status Report 22

Summary report for the Term: 22

Dates: 2 September 2022 - 9 September 2022

Start block: 2332800 0x2557284dd95b413b9a81486bb013bbd2242726e067e343f04a05667a8584ad98

End block: 2433600 0xda6e4ef47249398752f18164d72aa041aba7edf529e473b3e65bcd85b5cad488

WG Lead: yasir

WG Deputy 0x2bc 

## 1. 💵 Accounting

**Budget at the start of the term: 1.94** MtJOY
**Budget refilled during the term: 10.0** MtJOY
**Discretionary spendings**: 0.0 MtJOY
**Lead rewards: 2.12** MtJOY
**Worker rewards: 7.77** MtJOY
**Budget at the end of the term:** 2.05 MtJOY

## Group Changes

## 2. Group Changes

### Hires

- na

### Slashes

- na

### Firings

- na

## 3. Timesheet

This is based on self-reporting info

|  |  **Hours of Work** |  |
| --- | --- | --- |
| Worker ID 1 (joystreamstats) |  |  |
| Worker ID 2 (alexznet) |  |  |
| Worker ID 3 (maxlevush) |  |  |
| Worker ID 4 (l1dev) |  |  |
| Worker ID 5 (GodsHunter) |  |  |
| Worker ID 8 (mmx1916) |  |  |
| Worker ID 9 (Craci_BwareLabs) | 2 |  |
| Worker ID 10 (razumv) | 1 |  |
| Worker ID 11 (sieemma) | 2 |  |
| Worker ID 13 (plycho)  |  |  |
| Worker ID 14 (abramaria_) | 2 |  |
| Worker ID 15 (kalpacki) |  |  |
| Worker ID 16 - Lead (yyagi) | 25 |  |
| Worker ID 18 - Deputy Lead(0x2bc) | 4 |  |

**Lead Extra Hours: no**

## 4. Bounties for newcomers

- no new bounties (we are not looking for newcomers in the Storage WG!)

## 5. Notion Board Changes

- No changes

## 6. **List of completed tasks**

- Developed tasks required by the new Bonus system
- Maintained STORAGE_SCORE
- Carthage release testing is in progress
- Created documentation of lead activities.: [https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/leader](https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/leader)

## 7. **Ideas to improve your Working Group**

- Evicting a user should remove the bucket and bags associated, or force the admin to do the clean up before proceeding.
- Working on anew **Standard Operation procedure** :[https://github.com/yasiryagi/community-repo/blob/master/working-groups/storage-group/SOP/README.md](https://github.com/yasiryagi/community-repo/blob/master/working-groups/storage-group/SOP/README.md)

## 8. **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project
- Think of reducing documentation and automate data. Most requested data in this report can be automated.
- Raised or contributed to tickets to improve performance:
    - https://github.com/Joystream/joystream/issues/4274
    - https://github.com/Joystream/joystream/issues/4270

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

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%2015a000028df54de69bdeb0d668ac2d3b.csv)

# BUCKETS Info

# BUCKETS Info

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%20d5b82d6a6da44c1dacb5784a0543e235.csv)

## BUCKETS CREATED

Bucket Created: 0

## BUCKETS DELETED

Bucket Deleted: 0

## BAGS

Bags Created: 0

Bags Deleted: 0

# Lost Objects - GraphQL

Total Objects: 257

Total Lost Objects: 71

Percentage Lost Objects: %27.626459143968873

Test bag ID: YYAGI:2705,2706
Test bag ID: 0x2bc:2222, 2223, 2227

Excluding The test bags:

Total Objects: 234

Total Lost Objects: 49

Percentage Lost Objects: %20.9

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%2009ef8752db3943758bacb5b5b549d47a.csv)

# Objects Info during this Council Period

Total Objects Size: 123

Total Objects Size: 5238548334 bytes

## Objects Size Distribution

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%20f7f91c1bd83e496093ff1386358ae256.csv)

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%200de7cd8d30f4460eaf9a845a858a4142.csv)

## Objects Size Distribution Per Bag

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%2029a1df37b36f455eb25e8983c7934bcd.csv)

# Total object Info (Over all time)

Total Objects: 15769

Total Objects Size: 959895072627 bytes

Total Number of Bags in use: 651 bytes

Grand Total Number of Bags: 699 bytes

## Objects Size Distribution

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%20d0e63d87466849f8a0fce2b2f1c05b2d.csv)

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%20e3828fba9bf54bb49a8e2a34ffb8c885.csv)

## **Objects Size Distribution Per Bag**

[Untitled](Storage%20WG%20Status%20Report%2022/Untitled%204687b23af5ac4621a59556134889cc31.csv)

![Untitled](Storage%20WG%20Status%20Report%2022/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%2022/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%2022/Untitled%202.png)

# Elastic Search Logging

Connected nodes:

- ALEXZNET_SP
- joyrq_SP
- sieemma_SP
- 0x2bc_SP
- abramaria_SP
- YYAGI2_SP
- 3886-Craci_BwareLabs_SP
- razumv_SP

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

### user evicted

for i in $(seq 2000 2710) ; do     yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/keys/storage-role-key.json -r 8 -p xxxxxxxx; done
yarn storage-node leader:remove-operator -i 8 -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:delete-bucket -i 8 -k /path/to/storage-lead-role-key.json -p xxxxxxxx
yarn storage-node leader:delete-bucket -i 8 -k /root/keys/storage-role-key.json -p xxxxxxxx

### Node failed

yarn storage-node leader:update-bucket-status -i 9 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2000 -k /root/keys/storage-role-key.json -r 9 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2000 -k /root/keys/storage-role-key.json -r 9 -p xxxxxxxx

### Node failed

for i in $(cat ~/bags_pl_joystreamstats) ; do     yarn storage-node leader:update-bag -i $i -k /root/keys/storage-role-key.json -r 1 -p xxxxxxxx; done

### Node failed

yarn storage-node leader:update-bucket-status -i 6 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx

### upload testing

yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 17 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 17 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -a 17 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -r 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -r 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -r 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -a 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -a 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2213 -k /root/keys/storage-role-key.json -a 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2222 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2222 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 17 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2222 -k /root/keys/storage-role-key.json -r 2 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2222 -k /root/keys/storage-role-key.json -r 3 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2222 -k /root/keys/storage-role-key.json -r 14 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -a 16 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -r 17 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2706 -k /root/keys/storage-role-key.json -r 17 -p xxxxxxxx

yarn storage-node leader:update-bucket-status -i 16 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:update-bucket-status -i 16 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
for i in $(cat bags_file_16) ; do     yarn storage-node leader:update-bag -i $i -k /root/keys/storage-role-key.json -r 1 -p xxxxxxxx; done
for i in $(cat bags_file_16) ; do     yarn storage-node leader:update-bag -i $i -k /root/keys/storage-role-key.json -r 16 -p xxxxxxxx; done
yarn storage-node leader:update-bucket-status -i 16 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 1 -p xxxxxxxx
yarn storage-node leader:update-bag -i dynamic:channel:2705 -k /root/keys/storage-role-key.json -a 1 -p xxxxxxxx

[Current costs ](Storage%20WG%20Status%20Report%2022/Current%20costs%2035300913ca4f428bbfb826556abbf252.csv)

[](Storage%20WG%20Status%20Report%2022/Untitled%20e7c8a6e7c42a4cb48990eb0433f631c8.md)