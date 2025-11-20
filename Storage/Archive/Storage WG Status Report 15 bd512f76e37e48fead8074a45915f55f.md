# Storage WG Status Report 15

# **Summary**

**GENERAL_WG_SCORE**

Dates: 06 June 2022 - 13 July 2022

Summary report for the Term: 15

Start block: 1483200 0xa886f97c37ca5d3e67176a6430950819136974ea397b84fe84f1f02ba597b7ed

End block: 1598400

0x49a6766e201947b366bc9a4e0cf735f7b52120dfdc7fc3fa29aa04251858bbe1

WG Lead: 0x2bc

WG Deputy Lead: yasir

## Accounting

**Budget at the start of the term: 10.7871 MJOY**
**Workers rewards: `9.9128M tJOY`**
**Discretionary spendings**: **`0.000M tJOY`**
**Budget at the end of the term:** **`8.8743 MJOY`**

- Budget refilled during the term **8.0 M**

## Group Changes

### Hires

- No one was hired

Here are reasons behind that: 

<aside>
💡 1. No candidates
2. Also pay attention, now we have the COST_SCORE which appeared from the fact that we hired more people that we really needed (i told about that to Council many times). So JSG is basically asking why many people maintain costly hardware taking into account that this extra capacity *is not really needed*.
More discussions [here](https://discord.com/channels/811216481340751934/812344681786507274/995763117030117456)

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
| Worker ID 0 - Lead (0x2bc) | 14 |
| Worker ID 1 (joystreamstats) | 0 |
| Worker ID 2 (alexznet) | 1 |
| Worker ID 3 (maxlevush) | 2 |
| Worker ID 4 (l1dev) | 4 |
| Worker ID 5 (GodsHunter) | n/a |
| Worker ID 7 - Deputy Lead (yyagi) | 4 |
| Worker ID 8 (mmx1916) | n/a |
| Worker ID 9 (Craci_BwareLabs) | n/a |
| Worker ID 10 (razumv) | 1 |
| Worker ID 11 (sieemma) | n/a |
| Worker ID 13 (plycho)  |  |
| Worker ID 14 (abramaria_) | 2 |
| Worker ID 15 (kalpacki) | n/a |

Few people has no hours because they didn’t answer during 24 hours after my request

**Lead “Extra” Hours:**

- Research Score : 3**h**
- Cost score : 1**h**

## Bounties for newcomers

Entry level bounty 

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## Notion Board Changes

- updated the main page
- updated reports’ page

## **List of completed tasks**

- [LOGGING_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#logging_score): Keep improving the Elastic Search Report System
    - [ES bounty is developed](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md). Responsible worker is *yasir.*
- [RESEARCH_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#research_score): 80% completed.
    
    [Research Score Report](Storage%20WG%20Status%20Report%2015/Research%20Score%20Report%20c38669bd296f47cd8c88a688a0539e9e.md)
    
- COST_SCORE: 100% completed.
    
    [Costs Score Report](Storage%20WG%20Status%20Report%2015/Costs%20Score%20Report%20c251df242ecf49c7b786375d4d6b6430.md)
    
- Keep assisting the Deputy Lead. Current status of work:
    - Deputy Lead *keep* finializing automation of the Storage term report
    - Deputy Lead *keep* working on tuning up ES dashboards. See [the full task](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md)
- Worked with the Marketing/ HR to find more candidates to the group

## **Ideas to improve your Working Group**

- Make a decision how to balance between OPPORTUNITY SCORE and COST SCORE. See the discussion [here](https://discord.com/channels/811216481340751934/812344681786507274/995763117030117456). If one is improved, the other one will be degraded.
- Feedback on the scores is extremely helpful. Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.

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

[Bags’ Data](Storage%20WG%20Status%20Report%2015/Bags%E2%80%99%20Data%200989e7dadcb04a56a94d4bed7e84937f.csv)

- How many bags were created.
    - Number of bags created:  5
- How many bags were deleted.
    - Number of bags created:   0
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	127
    Number of Objects Lost:	                 20
    % of failed uploads	                          15.75%
    
    </aside>
    
    [Lost objects](Storage%20WG%20Status%20Report%2015/Lost%20objects%20c8752773149b44c392195935f2112593.csv)
    

<aside>
💽 We’ve lost 15% of objects. The 5-7% is a “usual” rate of loss which primarily accounted for network issues etc, and the rest 7-10% is accounted by the offline node ID=4 which i didn’t detected on a timely manner. 
Here I would suggest to create a notification system, i.e. telegram bot, which will alarm once  any of nodes go offline or once the failed upload events occur

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 127
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 12.72 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%205/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%206/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%207/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%208/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%209/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%2011/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%2012/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%2013/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%2014/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%2015/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%2015/Untitled%201.png)
    
- amount of bags;
    - Total amount of bags: **652**
    
    ![Untitled](Storage%20WG%20Status%20Report%2015/Untitled%202.png)
    
- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%2015/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%204bd178bf758e462ba758d421ccf804a9.csv)

- What is the current running costs for the system, and a breakdown of said costs.

**Total cost is 1054 USD**

[Current costs ](Storage%20WG%20Status%20Report%2015/Current%20costs%2088a2f74b461648a0aebd9358a552883a.csv)

- How much bandwidth did the individual nodes consume during the period.

 Every node transfers from 50 to 100 MB per day. As we use not really accurate measurement `ifconfig` tool, specific numbers per every noSide should not be used as a basis for decision marking.

- traffic consumption example (old)
    
    ![Untitled](Storage%20WG%20Status%20Report%2011/Untitled%204.png)
    

UPD 28 JUN 2022. We are now moving to a much more accurate measurement tool based on ES. Please see this [https://github.com/yasiryagi/elasticsearch-docker/tree/master/client](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client) This script measure CPU stats and traffic consumption stats and send it all to the ES platform managed by l1dev. [See the dashboard](https://kibana.joystreamstats.live/app/dashboards#/view/035e7f00-ecd0-11ec-8e8b-bffe711c3f6d?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:'2022-06-07T08:31:00.000Z',to:'2022-06-19T08:31:30.000Z')))  The work is still in progress

UPD 13 JUL 2022. We’ve got a good progress here since yasir applied for the bounty task aimed at improving of ES reporting  [https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md) 

![Untitled](Storage%20WG%20Status%20Report%2012/Untitled%203.png)

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 **NEW: we also got a new Discord bot that notified once the nodes go offline (not responded to the GET request)** 
    (1) On a daily basis: monitor status of the storage nodes [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload 
    (3) On a daily basis: monitor status of the storage nodes [https://kibana.joystreamstats.live/app/dashboards](https://kibana.joystreamstats.live/app/dashboards)
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) Make few uploading tests
          (2) Decrease stake amounts for all Storage Workers 
     
    
    yarn storage-node leader:update-bag -i dynamic:channel:2634 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 12 -p ****
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p 7WuZaFA419bO1 -i 14 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2634 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 14 -p ****
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p 7WuZaFA419bO1 -i 14 -s off
    
    ./cli/bin/run working-groups:updateWorkerReward 14 5
    ./cli/bin/run working-groups:decreaseWorkerStake 2 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 3 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 4 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 5 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 7 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 8 50000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 2 900000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 3 900000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 1 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 2 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 3 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 4 949000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 5 1000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 7 149000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 8 2200 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 9 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 10 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 11 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 13 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 14 49000 -g=storageProviders
    ./cli/bin/run working-groups:decreaseWorkerStake 15 49000 -g=storageProviders
    ./cli/bin/run working-groups:updateWorkerReward 15 5
    ./cli/bin/run working-groups:updateWorkerReward 2 6
    ./cli/bin/run working-groups:updateWorkerReward 3 6
    ./cli/bin/run working-groups:updateWorkerReward 4 6
    ./cli/bin/run working-groups:updateWorkerReward 5 6
    ./cli/bin/run working-groups:updateWorkerReward 7 10
    ./cli/bin/run working-groups:updateWorkerReward 8 6
    ./cli/bin/run working-groups:updateWorkerReward 9 6
    ./cli/bin/run working-groups:updateWorkerReward 10 6
    ./cli/bin/run working-groups:updateWorkerReward 11 6
    ./cli/bin/run working-groups:updateWorkerReward 13 6
    ./cli/bin/run working-groups:updateWorkerReward 14 6
    ./cli/bin/run working-groups:updateWorkerReward 15 6