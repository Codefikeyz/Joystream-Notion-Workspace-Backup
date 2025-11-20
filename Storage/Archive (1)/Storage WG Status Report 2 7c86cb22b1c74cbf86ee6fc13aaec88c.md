# Storage WG Status Report 2

4 April 2022 - 10 April 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 2nd report for the Storage Provider Working Group in Olympia.

- One more week without accidents
- Two new storage providers were onboarded

**Plan for the next term:**

(A)Come up with an idea & provide a solution how to collect data for the following topics:

1. List of failed data upload upload attempts on chain, and if possible to find out - why.
2. What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 List of objects is available here [https://joystreamstats.live/storage](https://joystreamstats.live/storage). Detailed explanation “why” will be presented with the next report. The work is in progress.
    
    </aside>
    
3. What was the capacity and utilization of each storage bucket at the beginning and end of the term (number and size of data objects).

(B) Complete onboarding of the the 2 new Storage providers.

(C) Adjust rewards following the change in the budget

(D) Prepare requirements for the performance tests 

**Report (extended)**

1. How many storage buckets were created
    
    <aside>
    💽 Buckets at 04-APR-2022:       5
    Buckets at 10-APR-2022:        7
    
                                   Created:      2
    
    </aside>
    
2. How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
3. How many bags were created.
    
    <aside>
    💽 Bags at 04-APR-2022:       2312
    Bags at 10-APR-2022:        2327
    
    Bags created: 15
    
    </aside>
    
4. How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
5. How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
    
    <aside>
    💽 64
    
    </aside>
    
    - what was their total size,
        
        <aside>
        💽 14.652 GB
        
        </aside>
        
    - what was the size distribution.
        
        ![Untitled](../Archive/Storage%20WG%20Status%20Report%202/Untitled.png)
        
6. A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size;
    
    ![Untitled](../Archive/Storage%20WG%20Status%20Report%202/Untitled%201.png)
    
    ![Untitled](../Archive/Storage%20WG%20Status%20Report%202/Untitled%202.png)
    
    - amount of bags;
    
    ![Untitled](../Archive/Storage%20WG%20Status%20Report%202/Untitled%203.png)
    
    - (average) number and size of data objects in a bag
    
    [(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%202/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20d1e84b00fa5e417a92781264ddf77007.csv)
    
7. What is the current running costs for the system, and a breakdown of said costs.
    
    <aside>
    💽 411 USD is a total cost per month
    
    Worker ID	 Joystream Name         	Server cost, USD		
    0	                    0x2bc	                           89$
    1	                    joystreamstats                75$
    2	                    alexznet		          81$
    3	                    maxlevush	                   60$
    4	                    l1dev		                   29$
    5	                    GodsHunter	                   54,5$
    7	                    yyagi	                            77$
    
    Following their suggestion l1dev and joystreamstats nodes are not getting rewarded
    
    </aside>
    
8. How much bandwidth did the individual nodes consume during the period.
    
    <aside>
    💽 To be calculated starting from the next report.
    
    </aside>
    
9. What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to donwload/upload
    
    </aside>
    
10. A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
    <aside>
    💽 # hiring new people
    
    yarn joystream-cli working-groups:fillOpening --openingId 5 --applicationIds 10
    yarn joystream-cli working-groups:fillOpening --openingId 6 --applicationIds 13
    yarn joystream-cli working-groups:fillOpening --openingId 9 --applicationIds 19
    yarn joystream-cli working-groups:fillOpening --openingId 8 --applicationIds 18
    
    # updating rewards according to the budget and performance of the workers
    
    run working-groups:updateWorkerReward 1 10
    run working-groups:updateWorkerReward 2 10
    run working-groups:updateWorkerReward 3 10
    run working-groups:updateWorkerReward 4 0
    
    # creating new buckets for new people
    
    yarn storage-node leader:create-bucket -a -i 5 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -n 20000 -s 1500000000000 
    yarn storage-node leader:create-bucket -i 5 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -n 20000 -s 2000000000000
    yarn storage-node leader:create-bucket -i 7 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -n 20000 -s 1500000000000 
    
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 3 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 5 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p *** -i 2 -s on
    
    # filling buckets with bags
    
    for i in $(seq 2000 2299) 
    do 
        yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ***  
        yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ***  
    done
    
    </aside>
    

[List of Workers](Storage%20WG%20Status%20Report%202/List%20of%20Workers%203b5f6cf1483b4dff9db891b4d9c92ec2.csv)