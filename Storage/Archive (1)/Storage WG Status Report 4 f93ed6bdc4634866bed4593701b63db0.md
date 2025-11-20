# Storage WG Status Report 4

23 April 2022 - 29 April 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 4th report for the Storage Provider Working Group in Olympia.

- One more week without incidents
- $100 subsidy for SPs was obtained [https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring#council-period-parameters](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring#council-period-parameters)
- Developed a script for automated collection of data for SP reporting [https://www.notion.so/joystream/Storage-Node-Reporting-Script-e5c4881eb32c467583e48c907b0eaf0a](Storage%20Node%20Reporting%20Script%20fbf17c27b86c4e5d87b8f9023a3b1233.md)
    - Script was set up for all workers except for #l1dev and #joystreamstats nodes

**Plan for the next term:**

Come up with an idea and provide a solution how to collect data for the following topics:

- Prepare requirements for performance tests
- Prepare requirements for a unified reporting system for SP and DP work groups

**Meeting with JSG:**

Proposed date and time:

- Monday 12-00 UTC
- Tuesday 12-00 UTC
- Wednesday 12-00 UTC

**Proposed bounties:**

See [https://www.notion.so/joystream/Storage-SP-Bounty-e67f6f6219de408f8af229d585e11ded](../Storage%20SP%20Bounty%20e67f6f6219de408f8af229d585e11ded.md)

[Group budget](Storage%20WG%20Status%20Report%204/Group%20budget%20a9a96625efea4e1e87b786aa46bf31da.csv)

**Report (extended)**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 23-APR-2022:       10
    Buckets at 29-APR-2022:      10
    
                                   Created:      0
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 23-APR-2022:        2343
    Bags at 29-APR-2022:        2566
    
    Bags created: 223
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	1100
    Number of Objects Lost:	                 187
    % of failed uploads	                          17%
    
    </aside>
    

[Objects permanently lost](Storage%20WG%20Status%20Report%204/Objects%20permanently%20lost%20357e05d08602445b87dc79520bb35dee.csv)

<aside>
💽 From 187 of objects lost, 164 objects are less than 10 MB. 
From 187 objects lost, 59 has non-empty media ID which means they were uploaded but probably lost after that (according to the comment of #l1dev) 

All in all, this issue with failed upload requires additional in-depth research. Taking into account that all buckets are replicated with 4 to 6 replication ratio, it’s very unlikely that all these nodes were working badly. I had a guess that there may be a code-driven problem (uploading code can be improved?).

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 1100
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 8.373 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled%201.png)
    
- amount of bags;
    
    <aside>
    💽        Total amount of bags: 2566
    
    </aside>
    

![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled%202.png)

- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag 23-29 APR](Storage%20WG%20Status%20Report%204/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%203844fd7f0bb14cd09d0b4774b9c02335.csv)

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

![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled%203.png)

       Comment: This is a traffic consumption  based on ifconfig output. 

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) increase replication rate from 4 to 6 for new objects
    
    <aside>
    💽 for i in $(seq 2340 2566)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    </aside>