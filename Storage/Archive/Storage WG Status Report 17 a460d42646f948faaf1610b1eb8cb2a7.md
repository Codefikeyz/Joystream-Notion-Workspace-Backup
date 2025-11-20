# Storage WG Status Report 17

# **Summary**

**GENERAL_WG_SCORE**

Summary report for the Term: 17

Dates: 23 June 2022 - 31 August 2022

Start block: 1742400 0x779e631f8e523873ce3dc2309f151683947d107152967c799f1d59fd50bbb764

End block: 1872000 0x95b1a493bf23a9c0b28301ff7cb487592beba9b881ec21de23cf46e655ca5fa5

WG Lead: 0x2bc

WG Deputy Lead: yasir

## Accounting

**Budget at the start of the term: 5.1753 M tJOY**

**Workers rewards: `12.3291M tJOY`**

**Discretionary spendings**: **`0.0000M tJOY` (2M tJoy was spent from the Council budget)**

**Budget at the end of the term:** **`2.8462 MJOY`**

- Budget refilled during the term **10.0M tJOY**

## Group Changes

### Hires

- No one was hired

Here are reasons behind that: 

<aside>
💡 Soon we will have a runtime upgrade which means that all workers will be fired and some of them will be hired again. No need to hire a worker few days before the new testnet

</aside>

- One new Storage Provider vacancy is still open (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-22](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-22))
- One storage vacancy is still waiting for ***bwhm*** (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14))

### Slashes

- No slashes

### Firings

- No firings

## Timesheet

This is based on self-reporting info

|  |  **Hours of Work** |
| --- | --- |
| Worker ID 0 - Lead (0x2bc) | 15 |
| Worker ID 1 (joystreamstats) |  |
| Worker ID 2 (alexznet) | 1 |
| Worker ID 3 (maxlevush) |  |
| Worker ID 4 (l1dev) | 15 |
| Worker ID 5 (GodsHunter) |  |
| Worker ID 7 - Deputy Lead (yyagi) | 20 |
| Worker ID 8 (mmx1916) |  |
| Worker ID 9 (Craci_BwareLabs) | 2 |
| Worker ID 10 (razumv) |  |
| Worker ID 11 (sieemma) | 5 |
| Worker ID 13 (plycho)  |  |
| Worker ID 14 (abramaria_) | 3 |
| Worker ID 15 (kalpacki) | 2 |

Few people has no hours because they didn’t answer during 24 hours after my request

## Bounties for newcomers

[New bounty](Bounty%20-%20Ideas%20How%20to%20Maintain%2024%207%20works%20for%20Stor%200054106abb9343dd99a510712d2c785e.md) 

## Notion Board Changes

- No

## **List of completed tasks**

- Developed tasks required by the new Bonus system
- Created Storage WG Deputy vacancy
- Keep educating the Deputy Lead about the Lead tasks
- Failed Server Notification Bot: Prepared requirements for a script that notifies in Discord about failed nodes. Tested the script.
- LOGGING_SCORE is completed
- COST_SCORE: feedback from the JSG is required
- Improved STORAGE_SCORE in terns of:
    - Number of  storage node provider with Query node set up
    - Number of  storage node that display their location coordinates, node storage capacity

## **Ideas to improve your Working Group**

- Remove worker opportunities score
- Feedback on the scores is extremely helpful. Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.

Not sure that i fully understand these Scores

- SYSTEM_SCORE:
    - All storage nodes display their location coordinates, node storage capacity and **caching** in the metadata (what is caching?)
    - All storage that has been in the working group for more than 1 week (100,800 blocks), must maintain their own query node, and **share the public url** in the metadata (where should it be shared?)

## **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project

# Report

**REPORT_SCORE**

- How many storage buckets were created
    - Number of storage buckets created: 0
- How many storage buckets were deleted
    - Number of storage buckets deleted: 0
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).

[Utilization of Storage Buckets](Storage%20WG%20Status%20Report%2017/Utilization%20of%20Storage%20Buckets%2079d0c1c43abb43a9913a760fc12a7804.csv)

- How many bags were created.
    - Number of bags created:  2
- How many bags were deleted.
    - Number of bags created:   0
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	306
    Number of Objects Lost:	                 135
    % of failed uploads	                          44.11% 
    Without 2604 channel stats, the actual failed object rate is **20%** which is look like a real number, taking into account hot fix of the two failed nodes.  I’ll ask 2604 owner, MWG, to change the person who makes uploads. Hopefully this is a very local problem that will vanish once the new worker start uploading objects.
    
    </aside>
    
    [Failed uploaded objects](Storage%20WG%20Status%20Report%2017/Failed%20uploaded%20objects%20cff2e7389c0044a083aded37d1625bf7.csv)
    

<aside>
💽 We’ve lost 44% of objects. There are 2 reasons. (1) This is a first time when we had 2 failed Storage Nodes, bucket ID=1 and bucket ID=4. The reasons is run of capacity and transfer to the other hosting provider. (2) Channel ID=2604 has about 52% of failed upload which is very unusual. See details:

</aside>

![Untitled](Storage%20WG%20Status%20Report%2017/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%2017/Untitled%201.png)

Without 2604 channel stats, the actual failed object rate is 20% which is look like a real number, taking into account hot fix of the failed nodes. 

I’ll ask 2604 owner, MWG to change the person who makes uploads. Hopefully this is a very local problem that will vanish once the new worker start uploading objects. 

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 306
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 9.79 GB
        
        </aside>
        
    - what was the size distribution.
    
    ![Untitled](Storage%20WG%20Status%20Report%2017/Untitled%202.png)
    
- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%2017/Untitled%203.png)
    

- amount of bags;
    - Total amount of bags: **662**
    
    ![Untitled](Storage%20WG%20Status%20Report%2017/Untitled%204.png)
    
- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%2017/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%208d194f5ac743417d82be40214fc6caf1.csv)

- What is the current running costs for the system, and a breakdown of said costs.

**Total cost is 1054 USD**

[Current costs ](Storage%20WG%20Status%20Report%2017/Current%20costs%20fd3b966690b64bab928f5d85fecb8c3a.csv)

- How much bandwidth did the individual nodes consume during the period.
    
    See here for traffic Analysis : 
    
    [https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Flows-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Flows-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))
    
    [https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Dashboard-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Packetbeat-Dashboard-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))
    
- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage nodes [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload 
    (3) On a daily basis: monitor status of the storage nodes
    
     [https://kibana.joystreamstats.live/app/dashboards](https://kibana.joystreamstats.live/app/dashboards)
    
    [https://kibana.joystreamstats.live/app/dashboards#/view/Metricbeat-system-overview-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)](https://kibana.joystreamstats.live/app/dashboards#/view/Metricbeat-system-overview-ecs?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-15m,to:now)))
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.

these commands were intended to remove all bags from the failed node

for i in $(seq 2000 2332) ; do
yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 4 -p 7WuZaFA419bO1
done

for i in $(seq 2340 2652) ; do
yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 4 -p 7WuZaFA419bO1
done

yarn storage-node leader:update-bag -i dynamic:channel:2337 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 4 -p 7WuZaFA419bO1