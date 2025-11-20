# Storage WG Status Report 12

Dates: 11 June 2022 - 17 June 2022

Full report for the Term: 12

Start block: 1152000

End block: 1252800

# **Summary**

**GENERAL_WG_SCORE**

Dates: 11 June 2022 - 17 June 2022

Summary report for the Term: 12

Start block: 1152000

End block: 1252800

## Accounting

**Budget at the start of the term:** 6.7314 MJOY
**Workers rewards: `6.0564M tJOY`**
**Discretionary spendings**: **`6.0564M tJOY`**
**Budget at the end of the term:** 8.6750 MJOY

- Budget refilled during the term 8.0 M

## Group Changes

### Hires

- Storage `Provider 11: lovedret` was hired.
- One new Storage Provider vacancy was created (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-16](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-16))
- One storage vacancy is still waiting for `@bwhm` (see [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14))

### Slashes

- No slashes

### Firings

- No firings

## Timesheet

this is based on **self-reporting** info

few people has no hours because they didn’t answer during 24 hours after my request

## Bounties for newcomers

New entry level bounty was developed for newcomers

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## Notion Board Changes

- Created bounty was for newcomers

[https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

## **List of completed tasks**

- One more week without incidents

Additional tasks:

- Hired 1 more worker
- Continued onboarding the new deputy
- Worked on the score improvement:

**PLAN_SCORE:** 

- Included in the plan the links for the working group openings
- Submitted the plan before the deadline (election block + 72h)

**SUMMARY_SCORE:** 

- Submitted the summary after the term ended and include the accounting information including the term end block

**WORKER_OPPORTUNITIES_SCORE:** 

- Hired 1 more worker (`lovedret`)

**BOUNTY_SCORE:** 

Entry level bounty was developed [https://www.notion.so/joystream/Bounty-Storage-WG-Entry-Level-74b13f81a32d4efb811f8259d6fbeee0](Bounty%20%5BStorage%20WG%5D%20%5BEntry%20Level%5D%2074b13f81a32d4efb811f8259d6fbeee0.md)

- Filled time estimation
- Filled oracle
- Made an *easier* bounty

**OPENING_SCORE:** 

- Included the newcomers bounty link
- Improved the opening questions

(see here [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-16](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-16))

**RESEARCH_SCORE:** 

- Developed a guide for the elastic logging research  (see [https://github.com/yasiryagi/elasticsearch-docker](https://github.com/yasiryagi/elasticsearch-docker))

**SYSTEM_SCORE:** 

- Changed the dynamic policy to 5
- Filled some information about the `emergency_score`:
    - Users do have at least 80% chance of being able to upload 1 object successfully, despite 2 storage nodes hypotethically being down. See my reasoning:
        - What we have: Currently replication rate is 5, the system has 6 active buckets that accept bags.
        - In our case: 2 storage nodes are down. In worst scenario, there are 3 uploading attempts, 2 of which were dropped by the down storage nodes.
        - Since I test all storage buckets (upload test) on a weekly basis and there is no problems observers, it seems that there is no other obstacles why user can’t upload his object on his 3rd attempt.

## **Ideas to improve your Working Group**

- Feedback on the Scores as @freakstatic did the last time was extremely helpful  [https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235](https://discord.com/channels/811216481340751934/812344681786507274/987280349740552235)
- Next time plz make the scores for the previous term to appear quicker. I.e. we received scores for the 11th term only on Friday. We couldn’t not show *best possible* the improvement of the scores in such circumstances.

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
    
    
    [Buckets Info](Storage%20WG%20Status%20Report%2012/Buckets%20Info%20702a689342b84ffaab9b075c9321bdee.csv)
    
- How many bags were created.more
    - Number of bags created:   5

- How many bags were deleted.
    - Number of bags created:   0
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	78 (yeah, the same as the last time!)
    Number of Objects Lost:	                 3
    % of failed uploads	                          3,8%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%2012/Permanently%20lost%20objects%20e43a2d1d04ba49cea5cb4ff83e8532f3.csv)
    

<aside>
💽 We’ve lost 3 objects, only one of those was a real video (ID=14640). The size of the other 2 objects is close to 0 MB which leads that they most probably consist some meta information rather real video files.  Object ID=14640 was later successfully reloaded. 

I’ve noticed that during previous months there were many problems with this particular bag (ID=2604). It seems that the owner of the channel may have poor internet connection that can be the root cause of the problem. 

Recommendation: communicate to the owner and check his internet connection quiality.

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 78
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 8.4 GB
        
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

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%2012/Untitled%201.png)
    
- amount of bags;
    - Total amount of bags: 637

![Untitled](Storage%20WG%20Status%20Report%2012/Untitled%202.png)

- (average) number and size of data objects in a bag

[Untitled](Storage%20WG%20Status%20Report%2012/Untitled%200c8cd9b0bd184f7495ed5751469a2a73.csv)

- What is the current running costs for the system, and a breakdown of said costs.
    
    <aside>
    💽 428 USD is a total cost per month
    
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
    
    </aside>
    

- How much bandwidth did the individual nodes consume during the period.

 Every node transfers from 50 to 100 MB per day. As we use not really accurate measurement `ifconfig` tool, specific numbers per every node should not be used as a basis for decision marking.

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
          (1) Hired one Storage Worker
          (2) Created 1 new Storage Worker vacancy
          (3) Created buckets for new emplyees      
          (4) Increased replication rate 
          (5) Increased dynamic replication policy to 5
     
    
    yarn storage-node leader:create-bucket -i 11 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -n 20000 -s 1500000000000
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 12 -s off
    
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 10 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2633 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 10 -p ***
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 10 -s off
    
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 11 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2634 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 11 -p ***
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 11 -s off
    
    yarn joystream-cli working-groups:fillOpening --openingId 13 --applicationIds 28
    
    yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ***
    
    for i in $(seq 2632 2636) ; do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ***
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ***
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ***
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ***
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ***
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ***
    done
    
    yarn joystream-cli working-groups:createOpening -g=storageProviders