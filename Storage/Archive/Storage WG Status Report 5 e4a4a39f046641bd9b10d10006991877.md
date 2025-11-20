# Storage WG Status Report 5

30 April 2022 - 6 May 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 4th report for the Storage Provider Working Group in Olympia.

- One more week without incidents
- Bounties for Storage WG were provided

**Plan for the next term:**

- I will continue the work on tasks from the last week.
    - Prepare requirements for performance tests
    - Prepare requirements for a unified reporting system for SP and DP work groups

**Proposed bounties:**

See [https://www.notion.so/joystream/Storage-SP-Bounty-e67f6f6219de408f8af229d585e11ded](../Storage%20SP%20Bounty%20e67f6f6219de408f8af229d585e11ded.md)

[Group budget](Storage%20WG%20Status%20Report%205/Group%20budget%203a34769cc88341e9ab6dfdce32e9d4c9.csv)

**Report (extended)**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 30-APR-2022:       10
    Buckets at 06-MAY-2022:      10
    
                                   Created:      0
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 30-APR-2022:        2566
    Bags at 06-MAY-2022:        2599
    
    Bags created: 34
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	186
    Number of Objects Lost:	                 10 (and 10 more lost  were “test” objects)
    % of failed uploads	                          5% (last term it was 17%)
    
    </aside>
    
    [Objects permanently lost](Storage%20WG%20Status%20Report%205/Objects%20permanently%20lost%201614bddabb7c463a803e440e6e468607.csv)
    

<aside>
💽 From these objects, only one with a size 21.6 MB subbosed to be a video. Later it was successfully uploaded with ID=141

All in all, this issue with failed upload requires additional in-depth research. I’m still working on this

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 186
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 4.8 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%205/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%205/Untitled%201.png)
    
- amount of bags;
    
    <aside>
    💽        Total amount of bags: 2566
    
    </aside>
    

![Untitled](Storage%20WG%20Status%20Report%205/Untitled%202.png)

- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%205/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20c5298c67cafa483485b070ff3f352412.csv)

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
    
    For information: joystreamstats, l1dev and mmx1916 are not getting paid in tJoy/Joy
    
    </aside>
    
- How much bandwidth did the individual nodes consume during the period.

![Untitled](Storage%20WG%20Status%20Report%205/Untitled%203.png)

       Comment: This is a traffic consumption  based on ifconfig output. 

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) update salaries of the workers
    
    <aside>
    💽 ./cli/bin/run working-groups:updateWorkerReward 1 5
    ./cli/bin/run working-groups:updateWorkerReward 4 5
    ./cli/bin/run working-groups:updateWorkerReward 8 5
    
    </aside>