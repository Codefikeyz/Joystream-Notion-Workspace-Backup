# Storage WG Status Report 6

7 May 2022 - 13 May 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 6th report for the Storage Provider Working Group.

- One more week without incidents
- Updated salaries of the workers according to the proposal [https://dao.joystream.org/#/proposals/preview/155](https://dao.joystream.org/#/proposals/preview/155)
(increase reward per operational node 2/block (0.2M))
- Introduce new bonus system [https://discord.com/channels/811216481340751934/812344681786507274/975317144403324978](https://discord.com/channels/811216481340751934/812344681786507274/975317144403324978)

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled.png)

**Plan for the next term:**

- I will continue the work on tasks from the last week.
    - Introduce new bandwidth measurement system instead of not accurate measurements with ifconfig utility
    - Raise priority of Storage WG bounties  by Builders WG

**Proposed bounties:**

See [https://www.notion.so/joystream/Storage-SP-Bounty-e67f6f6219de408f8af229d585e11ded](../Storage%20SP%20Bounty%20e67f6f6219de408f8af229d585e11ded.md)

[Group budget](Storage%20WG%20Status%20Report%206/Group%20budget%2097fd54a9499c46a0992c5153f465f424.csv)

**Report (extended)**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 07-MAY-2022:       9
    Buckets at 13-MAY-2022:        9
    
                                   Created:      0
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 07-MAY-2022:        2599
    Bags at 13-MAY-2022:        2607
    
    Bags created: 8
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	134
    Number of Objects Lost:	                 3 ( and 16 “test” objects from 2333 bag)
    % of failed uploads	                          2,2%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%206/Permanently%20lost%20objects%20e6645d69cffe4719b03e3de0874dd0c8.csv)
    

<aside>
💽 Except “test” objects, that were used by the Lead for testing purposes, 3 objects were lost: 14260, 14294 and 14296. (1) 14260 has 0 bytes size. (2) 14294 and 14296 have similar size which means that they are basically the same object.

In other words, only one object was lost. 
  
This issue with failed upload requires additional in-depth research. I’m still working on this. I’ve requested access to JavaScript errors from **klaudiusz.eth.** I believe this information will greatly help us to understand the origin of upload errors.

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 134
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 6.96 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%205/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled%201.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled%202.png)

- amount of bags;
    
    <aside>
    💽        Total amount of bags: 2566
    
    </aside>
    

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled%203.png)

- (average) number and size of data objects in a bag

[(average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%206/(average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20a2bb93ef11df478da78ca74a3abd9b2b.csv)

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
    
    </aside>
    
- How much bandwidth did the individual nodes consume during the period.

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled%204.png)

       Comment: This is a traffic consumption  based on ifconfig output. 

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) updated salaries of the workers according to the proposal [https://dao.joystream.org/#/proposals/preview/155](https://dao.joystream.org/#/proposals/preview/155)
             • increase reward per operational node 2/block (0.2M)
    
    <aside>
    💽 ./cli/bin/run working-groups:updateWorkerReward 8 12
    ./cli/bin/run working-groups:updateWorkerReward 7 12
    ./cli/bin/run working-groups:updateWorkerReward 5 12
    ./cli/bin/run working-groups:updateWorkerReward 4 12
    ./cli/bin/run working-groups:updateWorkerReward 3 12
    ./cli/bin/run working-groups:updateWorkerReward 2 12
    ./cli/bin/run working-groups:updateWorkerReward 1 12
    
    </aside>