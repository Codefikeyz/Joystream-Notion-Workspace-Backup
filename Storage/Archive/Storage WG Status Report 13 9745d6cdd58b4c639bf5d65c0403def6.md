# Storage WG Status Report 13

# **Summary**

**GENERAL_WG_SCORE**

Dates: 19 June 2022 - 28 June 2022

Summary report for the Term: 13

Start block: 1,252,800

End block: 1,382,400

WG Lead: 0x2bc

## Accounting

**Budget at the start of the term:** 8.6750 MJOY
**Workers rewards: `8.0816M tJOY`**
**Discretionary spendings**: **`0M tJOY`**
**Budget at the end of the term:** 10.5934 MJOY

- Budget refilled during the term 10.0 M

## Group Changes

### Hires

- Storage Provider `plycho` was hired.
- Storage Provider  `abramaria_` was hired.
- One new Storage Provider vacancy was created (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-16](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-18))
- One storage vacancy is still waiting for `@bwhm` (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14))

### Slashes

- No slashes

### Firings

- Storage Provider  `lovedret` was fired. He didn’t appeared within a week after his hiring.

## Timesheet

This is based on self-reporting info

|  | **Work Hours** |
| --- | --- |
| Worker ID 0 - Lead (0x2bc) | 15 |
| Worker ID 1 (joystreamstats) | 0 |
| Worker ID 2 (alexznet) | 2 |
| Worker ID 3 (maxlevush) | 3 |
| Worker ID 4 (l1dev) | 2 |
| Worker ID 5 (GodsHunter) | n/a |
| Worker ID 7 - Deputy Lead (yyagi) | n/a |
| Worker ID 8 (mmx1916) | 5 |
| Worker ID 9 (Craci_BwareLabs) | 5 |
| Worker ID 10 (razumv) | 2 |
| Worker ID 11 (sieemma) | 5 |
| Worker ID 13 (plycho)  |  |
| Worker ID 14 (abramaria_) | new worker |

Few people has no hours because they didn’t answer during 24 hours after my request

## Bounties for newcomers

New entry level bounty was developed for newcomers

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## Notion Board Changes

Bounty  for newcomers is in place

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## **List of completed tasks**

- Keep educating the deputy about the lead tasks
    - Deputy Lead (yyagi) got familiar with the main parts of the Storage Report. He is automating it with Python scripts now.
- Worked with the Marketing/ HR to find more candidates to the group
- Hired two more workers, *plycho* and *abramaria_*
- Keep improving the “Elastic Report System” ([LOGGING_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#logging_score))
    
    - Setup and configurations: manuals are available [here](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client) and [here](https://github.com/yasiryagi/elasticsearch-docker/) 
    - Extracting and parsing the data: dashboard is available [here](kibana.joystreamstats.live/app/dashboards). You can ask credentials from *l1dev*
    - What it provides for a Lead: online convinient access to the logs erros and info messages. 
    
    ![Untitled](Storage%20WG%20Status%20Report%2013%20-%20Summary%20(1)/Untitled.png)
    
    - Operators to report to it. Here is a list:
    
    | **Worker** | **Reported to the ES** |
    | --- | --- |
    | Worker ID 0 - Lead (0x2bc) | YES |
    | Worker ID 1 (joystreamstats) | YES |
    | Worker ID 2 (alexznet) | YES |
    | Worker ID 3 (maxlevush) | YES |
    | Worker ID 4 (l1dev) | YES |
    | Worker ID 5 (GodsHunter) | - |
    | Worker ID 7 - Deputy Lead (yyagi) | - |
    | Worker ID 8 (mmx1916) | - |
    | Worker ID 9 (Craci_BwareLabs) | - |
    | Worker ID 10 (razumv) | YES |
    | Worker ID 11 (sieemma) | YES |
    
    | Worker ID 14 (abramaria_) | new worker |
- Cancel old working group openings (ID: 14, 16 or 17 - keep one of them)
    - Done. Working group openings 16 and 17 are liquidated.
- Keep working on the ([RESEARCH_SCORE](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#research_score))
    - Work is in progress
- Make sure all storage node logs are available and that is possible to extract some useful information about the system.
    - Check the information above in the LOGGING_SCORE section.

## **Ideas to improve your Working Group**

- Feedback on the Scores as @freakstatic did the last time was extremely helpful  [https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235](https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235)
- Next time please make the scores for the previous term to appear quicker. So we will be able to work more efficiently during the term.

## **Ideas to improve other Working Group, Council, Jsgenesis**

- To conduct Leads meeting to increase level of collaboration and understanding what’s going on in the project

# Report

**REPORT_SCORE**

- How many storage buckets were created
    - Number of storage buckets created: 2
- How many storage buckets were deleted
    - Number of storage buckets deleted:   0
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).

![Untitled](Storage%20WG%20Status%20Report%2013/Untitled.png)

- How many bags were created.
    - Number of bags created:   5
- How many bags were deleted.
    - Number of bags created:   0
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	93
    Number of Objects Lost:	                 7
    % of failed uploads	                          7,5%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%2013/Permanently%20lost%20objects%20b55355be50b94c78ba3b75e9628ed5c3.csv)
    

<aside>
💽 We’ve lost 7 objects, 2 of which with size close to 0 MB. The majority of objects, 6/7, were uploaded to the 2604 channel which is the official Channel of Marketing WG. 

I closely communicate with MWG, specifically with SwarGo, to reproduce the situation. At first, it looks like a problem with specific PC/software that is used by SwarGo.

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 101
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 6.54 GB
        
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

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%2013/Untitled%202.png)
    
- amount of bags;
    - Total amount of bags: **642**
    
    ![Untitled](Storage%20WG%20Status%20Report%2013/Untitled%203.png)
    
- (average) number and size of data objects in a bag

[(average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%2013/(average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%204e7a69ea6c6a4b0cb3ad3a57084423b1.csv)

- What is the current running costs for the system, and a breakdown of said costs.
    
    <aside>
    💽 521 USD is a total cost per month
    
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
    11                        sieemma                             TBD
    13                        plycho                                TBD
    14                        abramaria_                        60$
    
    </aside>
    

- How much bandwidth did the individual nodes consume during the period.

 Every node transfers from 50 to 100 MB per day. As we use not really accurate measurement `ifconfig` tool, specific numbers per every noSide should not be used as a basis for decision marking.

- traffic consumption example (old)
    
    ![Untitled](Storage%20WG%20Status%20Report%2011/Untitled%204.png)
    

We are now moving to a much more accurate measurement tool based on ES. Please see this [https://github.com/yasiryagi/elasticsearch-docker/tree/master/client](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client) This script measure CPU stats and traffic consumption stats and send it all to the ES platform managed by l1dev. [See the dashboard](https://kibana.joystreamstats.live/app/dashboards#/view/035e7f00-ecd0-11ec-8e8b-bffe711c3f6d?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:'2022-06-07T08:31:00.000Z',to:'2022-06-19T08:31:30.000Z')))  The work is still in progress 

![Untitled](Storage%20WG%20Status%20Report%2012/Untitled%203.png)

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) Hired two Storage Worker
          (2) Created 1 new Storage Worker vacancy
          (3) Created 2 buckets for new employees      
     
    
    yarn joystream-cli working-groups:createOpening -g=storageProviders
    
    yarn joystream-cli working-groups:fillOpening --openingId 16 --applicationIds 30
    yarn joystream-cli working-groups:fillOpening --openingId 17 --applicationIds 29
    
    yarn storage-node leader:create-bucket -i 13 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ** -n 20000 -s 1500000000000
    yarn storage-node leader:create-bucket -i 14 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ** -n 20000 -s 1500000000000
    
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ** -i 13 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ** -i 14 -s off