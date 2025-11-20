# Storage WG Status Report 8

21 May 2022 - 27 May 2022

**Storage Lead : *0x2bc***

## Overview

- One more week without incidents
- Hired Deputy Lead @**yasir** and Storage Worker @**craci | [bwarelabs.com](http://bwarelabs.com)**

FYI [**bwarelabs.com](http://bwarelabs.com)**  is a first *specialised node team* in the Storage Group. This is quite a qood sign!

- Updated Storage WG budget according to @**freakstatic** input
- 5/8 workers installed traffic analysis script
- Initiated work on improvement of Research Score [analysed standard DEBUG messages of Storage Node logs]

**Proposed bounties:**

See [https://www.notion.so/joystream/Storage-SP-Bounty-e67f6f6219de408f8af229d585e11ded](../Storage%20SP%20Bounty%20e67f6f6219de408f8af229d585e11ded.md)

# **Summary**

**GENERAL_WG_SCORE**

- Accounting of how much was spent on what.
    - 8 MtJoy was paid as a remuneration to Storage Workers
    
    [Group budget (1)](Storage%20WG%20Status%20Report%208/Group%20budget%20(1)%20b6fcf7a01bbf47d986f6d8b340b6541d.csv)
    
- Actual hires made.
    - Hired Deputy Lead @**yasir**
    - Hired Storage Worker @**craci | [bwarelabs.com](http://bwarelabs.com)**
- Actual slashes imposed
    - Right now worker ID=5 is slashed for not updating his Traffic Analyzer script on time
- Actual firings done.
    - No
- Changes made to the corresponding notion board.
    - Added Storage WG Report 8 [https://www.notion.so/joystream/Storage-WG-Status-Report-8-bcd6ffb4bb414887b5f7ee8d0752bab2](Storage%20WG%20Status%20Report%208%20bcd6ffb4bb414887b5f7ee8d0752bab2.md)
- A summary on how well the working group served it's intended purpose.
    - One more week without incidents
    - WG worked quite well with failed uploaded object ration close to 1%
- Recommendations for what should be focused on in next council period in order to make group more effective.
    - Improving of Research Score
    - Hiring of 1 more Storage Worker
    - Onboarding already hired Deputy Lead and Storage Worker
- Suggested changes to the purpose or practices built in to this working group, other working groups, the council or Jsgenesis' role, in order to increase overall effectiveness of the group or the project.
    - No

# Report

**REPORT_SCORE**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 21-MAY-2022:       9
    Buckets at 27-MAY-2022:        9
    
                                   Created:      0
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 21-MAY-2022:        2623
    Bags at 27-MAY-2022:        2626
    
    Bags created: 3
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	67
    Number of Objects Lost:	                 1 
    % of failed uploads	                          1,4%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%208/Permanently%20lost%20objects%20db7fff86152b44f0a0a662cb9979e6c0.csv)
    

<aside>
💽 We’ve lost only 1 object with size of 0.01 MB

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 67
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 3.7 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%205/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%206/Untitled%201.png)

![Untitled](Storage%20WG%20Status%20Report%207/Untitled.png)

![Untitled](Storage%20WG%20Status%20Report%208/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%208/Untitled%201.png)
    
- amount of bags;
    
    <aside>
    💽        Total amount of bags: 627
    
    </aside>
    

![Untitled](Storage%20WG%20Status%20Report%208/Untitled%202.png)

- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%208/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%2095c986fdc5854e26a957ecd4e0d686a0.csv)

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
    9                          Craci_BwareLabs             TBD
    
    </aside>
    
- How much bandwidth did the individual nodes consume during the period.

![Untitled](Storage%20WG%20Status%20Report%208/Untitled%203.png)

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) hired Storage Worker
          (2)created new Storage Worker vacancy
          (3) updated Storage WG budget
     
    
    <aside>
    💽 ./cli/bin/run working-groups:updateWorkerReward 1 8
    ./cli/bin/run working-groups:updateWorkerReward 2 8
    ./cli/bin/run working-groups:updateWorkerReward 3 8
    ./cli/bin/run working-groups:updateWorkerReward 4 12  // do additional work
    ./cli/bin/run working-groups:updateWorkerReward 5 4   // don't respond
    ./cli/bin/run working-groups:updateWorkerReward 7 8
    ./cli/bin/run working-groups:updateWorkerReward 8 8
    ./cli/bin/run working-groups:updateWorkerReward 9 4
    
    yarn joystream-cli working-groups:fillOpening --openingId 10 --applicationIds 24
    
    joystream-cli working-groups:createOpening -g=storageProviders
    
    </aside>