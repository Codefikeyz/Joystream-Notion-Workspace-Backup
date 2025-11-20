# Storage WG Status Report 7

14 May 2022 - 20 May 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 7th report for the Storage Provider Working Group.

- One more week without incidents
- Had a call with **bwhm** on current status and future tasks
- Improved following SCORES
    - General WG Score
        - Added 1 new vacancy and planned 3 more new vacancies
        - Added Deputy Lead vacancy
    - Report Score
        - New bandwidth measurement system is introduced  (see latest paragraph) [https://www.notion.so/joystream/Storage-Node-Reporting-Script-e5c4881eb32c467583e48c907b0eaf0a](Storage%20Node%20Reporting%20Script%20e5c4881eb32c467583e48c907b0eaf0a.md)
    - Replication Rate score was revise and then increased. *I explained **bwhm** that ****all tests bags will be excluded from the calculation of  Replication Rate. He agreed on that.*

 **Plan for the next term:**

- Improvement of the Research Score

**Proposed bounties:**

See [https://www.notion.so/joystream/Storage-SP-Bounty-e67f6f6219de408f8af229d585e11ded](../Storage%20SP%20Bounty%20e67f6f6219de408f8af229d585e11ded.md)

[Group budget](Storage%20WG%20Status%20Report%207/Group%20budget%20822618902ad44ead8b69f1329008aeca.csv)

**Report (extended)**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 14-MAY-2022:       9
    Buckets at 20-MAY-2022:        9
    
                                   Created:      0
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 14-MAY-2022:        2607
    Bags at 20-MAY-2022:        2623
    
    Bags created: 16
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	71
    Number of Objects Lost:	                 1 
    % of failed uploads	                          1,4%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%207/Permanently%20lost%20objects%20d85b497e14114ff0bf394dca322aac62.csv)
    

<aside>
💽 We’ve lost only 1 object with size of 0.01 MB

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 71
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 5.1 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%205/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%206/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%207/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%207/Untitled%201.png)
    
- amount of bags;
    
    <aside>
    💽        Total amount of bags: 2623
    
    </aside>
    

![Untitled](Storage%20WG%20Status%20Report%207/Untitled%202.png)

- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%207/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20d52f55e6f04f4fada1e8311b4171a79c.csv)

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

![Untitled](Storage%20WG%20Status%20Report%207/Untitled%203.png)

       Comment: This is a traffic consumption  based on ifconfig output. 

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) created opening for the Storage Provider role
    
    <aside>
    💽 joystream-cli working-groups:createOpening -g=storageProviders
    
    </aside>