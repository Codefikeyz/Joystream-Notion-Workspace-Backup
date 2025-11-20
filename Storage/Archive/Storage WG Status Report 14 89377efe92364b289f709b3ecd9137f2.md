# Storage WG Status Report 14

# **Summary**

**GENERAL_WG_SCORE**

Dates: 28 June 2022 - 05 July 2022

Summary report for the Term: 14

Start block: 1382400 0xff9143bcf1f5ba78d4cb76e45bfc3b213b2dc0306775a44a307be0b75b701695

End block: 1483200

0xa886f97c37ca5d3e67176a6430950819136974ea397b84fe84f1f02ba597b7ed

WG Lead: 0x2bc

WG Deputy Lead: yasir

## Accounting

**Budget at the start of the term: 10.5934 MJOY**
**Workers rewards: `7.1737M tJOY`**
**Discretionary spendings**: **`0.000M tJOY`**
**Budget at the end of the term:** **10.7871 MJOY**

- Budget refilled during the term **7.0 M**

Comment: I’ve approved [the bounty](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md) for the Deputy Lead and increased the rewards for active workers by 1 tJoy. Next term we would probably have deficit of the budget.

## Group Changes

### Hires

- Storage Provider ***kalpakci*** was hired.
- One new Storage Provider vacancy was created (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-22](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-22)) enhanced by new markup
- One storage vacancy is still waiting for ***bwhm*** (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14))

### Slashes

- No slashes

### Firings

- No firings

## Timesheet

This is based on self-reporting info

|  |  **Hours of Work** |
| --- | --- |
| Worker ID 0 - Lead (0x2bc) | 12 |
| Worker ID 1 (joystreamstats) | n/a |
| Worker ID 2 (alexznet) | n/a |
| Worker ID 3 (maxlevush) | 3 |
| Worker ID 4 (l1dev) | n/a |
| Worker ID 5 (GodsHunter) | n/a |
| Worker ID 7 - Deputy Lead (yyagi) | 25 |
| Worker ID 8 (mmx1916) | n/a |
| Worker ID 9 (Craci_BwareLabs) | n/a |
| Worker ID 10 (razumv) | 3 |
| Worker ID 11 (sieemma) | 4 |
| Worker ID 13 (plycho)  |  |
| Worker ID 14 (abramaria_) | 10 |
| Worker ID 15 (kalpacki) | new worker |

Few people has no hours because they didn’t answer during 24 hours after my request

## Bounties for newcomers

New entry level bounty was developed for newcomers

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## Notion Board Changes

New bounty for ES is in place 

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md)

## **List of completed tasks**

- Keep assisting the Deputy Lead. Current status of work:
    - Deputy Lead finializes automation of the Storage term report
    - Deputy Lead started his work on tuning up ES dashboards. See [the full task](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md)
- Worked with the Marketing/ HR to find more candidates to the group
- Hired one more worker,  *kalpakci*
- Keep onboarding all new workers: setting up reporting for the nodes, making uploading tests
- [LOGGING_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#logging_score): Keep improving the Elastic Search Report System
    - [ES bounty is developed](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md). Work on the task is in progress. The responsible worker is *yasir*.
- [RESEARCH_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#research_score): Keep working on the.  Task completion is about 60%.

## **Ideas to improve your Working Group**

- Feedback on the Scores as @freakstatic did the last time was extremely helpful  [https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235](https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235)
- Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.

## **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project

# Report

**REPORT_SCORE**

- How many storage buckets were created
    - Number of storage buckets created: 1
- How many storage buckets were deleted
    - Number of storage buckets deleted:   0
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).

![Untitled](Storage%20WG%20Status%20Report%2014/Untitled.png)

- How many bags were created.
    - Number of bags created:  6
- How many bags were deleted.
    - Number of bags created:   0
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	54
    Number of Objects Lost:	                 4
    % of failed uploads	                          7,4%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%2014/Permanently%20lost%20objects%2078d035480c0746868ab477207492418d.csv)
    

<aside>
💽 We’ve lost 4 objects. Objects 14793, 14796 and 14807 were lost to misconfiguration of bags 2641 and 2642. Not that’s fixed. Object 14834 was lost while uploading to the bag 2604 which is well-known to be a “problem” bag. I still think that there is a poor internet connection issue associated with uploads for channel 2604. Once the ES reporting is finished we will know that for sure.

For information: 2604 bag is an official channel of Marketing WG.

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 54
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 8.23 GB
        
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

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%2014/Untitled%202.png)
    
- amount of bags;
    - Total amount of bags: **648**
    
    ![Untitled](Storage%20WG%20Status%20Report%2014/Untitled%203.png)
    
- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%2014/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20a2279b3b6f414bf0859b7b5d3ac623dd.csv)

- What is the current running costs for the system, and a breakdown of said costs.
    
    <aside>
    💽 908 USD is a total cost per month
    
    Worker ID	 Joystream Name         	Server cost, USD		
    0	                    0x2bc	                           89$
    1	                    joystreamstats                75$
    2	                    alexznet		          81$
    3	                    maxlevush	                   60$
    4	                    l1dev		                   29$
    5	                    GodsHunter	                   54,5$
    7	                    yyagi	                            77$ 
    8                          mmx1916                          17$ 
    9                          Craci_BwareLabs             110$
    10                        razumv                               33$
    11                        sieemma                             313$ (that’s correct!)
    13                        plycho                                74$
    14                        abramaria_                        60$
    15                         kalpakci                             TBD
    
    </aside>
    

- How much bandwidth did the individual nodes consume during the period.

 Every node transfers from 50 to 100 MB per day. As we use not really accurate measurement `ifconfig` tool, specific numbers per every noSide should not be used as a basis for decision marking.

- traffic consumption example (old)
    
    ![Untitled](Storage%20WG%20Status%20Report%2011/Untitled%204.png)
    

UPD 28 JUN 2022. We are now moving to a much more accurate measurement tool based on ES. Please see this [https://github.com/yasiryagi/elasticsearch-docker/tree/master/client](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client) This script measure CPU stats and traffic consumption stats and send it all to the ES platform managed by l1dev. [See the dashboard](https://kibana.joystreamstats.live/app/dashboards#/view/035e7f00-ecd0-11ec-8e8b-bffe711c3f6d?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:'2022-06-07T08:31:00.000Z',to:'2022-06-19T08:31:30.000Z')))  The work is still in progress

UPD 5 JUL 2022. We’ve got a good progress here since yasir applied for the bounty task aimed at improving of ES reporting  [https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20Elastic%20Search%20Development%208f42df9c4f00448cab8576aa5179761d.md) 

![Untitled](Storage%20WG%20Status%20Report%2012/Untitled%203.png)

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage nodes [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload 
    (3) On a daily basis: monitor status of the storage nodes [https://kibana.joystreamstats.live/app/dashboards](https://kibana.joystreamstats.live/app/dashboards)
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) Hired one Storage Worker
          (2) Created 1 new Storage Worker vacancy
          (3) Updated worker’s rewards
          (4) Maintain high replication rate      
     
    
    working-groups:cancelOpening 14
    yarn joystream-cli working-groups:overview -g=storageProviders
    
    ./cli/bin/run working-groups:updateWorkerReward 2 5
    ./cli/bin/run working-groups:updateWorkerReward 3 5
    ./cli/bin/run working-groups:updateWorkerReward 4 9
    ./cli/bin/run working-groups:updateWorkerReward 5 5
    ./cli/bin/run working-groups:updateWorkerReward 7 9
    ./cli/bin/run working-groups:updateWorkerReward 8 5
    ./cli/bin/run working-groups:updateWorkerReward 9 5
    ./cli/bin/run working-groups:updateWorkerReward 10 5
    ./cli/bin/run working-groups:updateWorkerReward 11 5
    ./cli/bin/run working-groups:updateWorkerReward 13 5
    
    yarn  joystream-cli working-groups:createOpening -g=storageProviders
    yarn joystream-cli working-groups:fillOpening --openingId 13 --applicationIds 28
    
    yarn  joystream-cli working-groups:createOpening -g=storageProviders
    yarn joystream-cli working-groups:fillOpening --openingId 18 --applicationIds 31
    
    yarn  joystream-cli working-groups:cancelOpening 21
    yarn joystream-cli working-groups:fillOpening --openingId 18 --applicationIds 31
    
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ***** -i 12 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2634 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 12 -p *****
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ***** -i 12 -s off
    
    for i in $(seq 2637 2644) ; do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p *****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p *****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p *****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p *****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p *****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p *****
    done
    
    yarn storage-node leader:create-bucket -i 15 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ***** -n 20000 -s 1500000000000 -a off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ***** -i 15 -s off