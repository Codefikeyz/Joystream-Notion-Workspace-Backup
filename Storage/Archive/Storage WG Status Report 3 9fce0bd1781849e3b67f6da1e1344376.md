# Storage WG Status Report 3

11 April 2022 - 22 April 2022

**Storage Lead : *0x2bc***

**Report:**
This is the 3rd report for the Storage Provider Working Group in Olympia.

- This report is for a longer period than usual in order to be in line with Distributor’s report.
- This week we have Validating node’s issue that lasted for one day and affect work of the Storage WG.
- There was an uploading issue with some objects which was caused by one buggy node and one node with poor internet connection. Now dynamic-bag-policy is set to 4 which helps to prevent such situations in the future.
- Seven bags were created for testing purposes (2333,2334,2335,2336,2337,2338,2339). All upload errors which relate to these bags should be excluded from the UPLOAD_SCORE. Replication rate for these test bags is set to 1 and it should not be counted during calculation of MAINTENANCE_SCORE.
- One more worker was hired (name: MMX). He was onboarded on a volunteer basis which mean he will not get paid.

**Plan for the next term:**

Come up with an idea and provide a solution how to collect data for the following topics:

- Develop a script for automatic collection of the stored objects from the SP workers
- Develop a script for automatic collection of the network consumption data from the SP workers
- Prepare requirements for performance tests

Meeting with JSG. 

Proposed date and time:

- Monday 12-00 UTC
- Tuesday 12-00 UTC
- Wednesday 12-00 UTC

[Group budget](Storage%20WG%20Status%20Report%203/Group%20budget%20e0cfb4978e684b0a8c729258caef0f21.csv)

**Report (extended)**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 11-APR-2022:       7
    Buckets at 22-APR-2022:      10
    
                                   Created:      3
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽 Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 11-APR-2022:         2327
    Bags at 22-APR-2022:        2342
    
    Bags created: 15
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Objects permanently lost: 9 (IDs: 12861, 12839, 12840, 12841, 12842, 12843, 12798, 12799, 12800). 
    
    See detailed stats here: [https://docs.google.com/spreadsheets/d/14h6J5Rxlzc4Qx64-7a7nTWzL4TOooObI6UfpyxkRbOM/edit#gid=1165833353](https://docs.google.com/spreadsheets/d/14h6J5Rxlzc4Qx64-7a7nTWzL4TOooObI6UfpyxkRbOM/edit#gid=1165833353)
    
    </aside>
    
    ![Untitled](Storage%20WG%20Status%20Report%203/Untitled.png)
    
    ![Untitled](Storage%20WG%20Status%20Report%203/Untitled%201.png)
    

<aside>
💽 Comment:
Objects were lost during the buggy configuration of the following nodes: BucketID=4,  BucketID=0. The situation was fixed in a timely manner: nodes were re-configured, dynamic-bag-policy was set to 4 (from 2) in order to avoid such situations in the future.

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 126 (or 117 if lost objects are not taken into account)
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 4.513 GB
        
        </aside>
        
    - what was the size distribution.
    
    ![Untitled](Storage%20WG%20Status%20Report%203/Untitled%202.png)
    
- How many data objects were (attempted) uploaded, and
    
    List of failed data upload attempts on chain, and if possible to find out - why.
    
    <aside>
    💽 See Section: “What data objects were permanently lost, and if any, why.”
    
    Please also take into consideration:
    
    > regardning MAINTENANCE_SCORE and UPLOAD_SCORE.
    (1) we have some test bags  (2233 to 2339) which are bounded to only 1 bucket each
    (2) we performed some stress test and few objects from these test buckets had uploading errors
    > 
    </aside>
    
- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](Storage%20WG%20Status%20Report%203/Untitled%203.png)
    
- amount of bags;

<aside>
💽        Total amount of bags: 2342

</aside>

![Untitled](Storage%20WG%20Status%20Report%203/Untitled%204.png)

- (average) number and size of data objects in a bag

[(Average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%203/(Average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%2028619534531946aa88ca84a431a5c874.csv)

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
    
    ![Untitled](Storage%20WG%20Status%20Report%203/Untitled%205.png)
    
    Comment: This is a very rough traffic consumption  based on ifconfig output. The approach to be improved soon. 
    
- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) Updated salaries according to the budget 
          (2) Fixed situation with failed upload object by re-configuring buckets and setting dynamic-bag-policy to 4  
          (3) Updated replication rate for all buckets 
          (4) Created 7 test bags (2333, 2334, 2335, 2336, 2337, 2338, 2339) 
    
           See commands below:
    
    <aside>
    💽 for i in $(seq 2000 2299)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 7 -p ****
    done
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2010)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 7 -p ****
    done
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 7 -s off
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:create-bucket -i 7 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -n 20000 -s 1500000000000
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s off
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2010)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 7 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s on
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2010)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s off
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2410)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2323 2323)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 0 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 1 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 3 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 4 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 5 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 6 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 7 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s off
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2299 2340)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 0 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 1 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 3 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 4 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 5 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 6 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 7 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s off
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 1 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 3 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 4 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 6 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s on
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bag -i dynamic:channel:2333 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 0 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2334 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2335 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2336 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2337 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2338 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2339 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 1 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 3 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 4 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 5 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 6 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 7 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s off
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bag -i dynamic:channel:2333 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2333 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2334 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2335 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2336 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2336 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2337 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2337 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2338 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2338 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2339 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:2339 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 2 -p ****
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 1 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 2 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 3 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 4 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 5 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 6 -s on
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 7 -s off
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 8 -s on
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 4 -k /root/.local/share/joystream-cli/accounts/SPLeader.json  -p ****
    yarn storage-node leader:create-bucket -i 7 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -n 20000 -s 1000000000000
    
    </aside>
    
    <aside>
    💽 ./cli/bin/run working-groups:updateWorkerReward 7 10
    ./cli/bin/run working-groups:updateWorkerReward 5 10
    ./cli/bin/run working-groups:updateWorkerReward 1 1
    
    </aside>
    
    <aside>
    💽 disable bucket 0 for some time
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2332)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -r 0 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:delete-bucket -i 5 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ****
    yarn storage-node leader:delete-bucket -i 7 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p ****
    
    </aside>
    
    <aside>
    💽 for i in $(seq 2000 2332)
    do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:create-bucket -i 8 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -n 20000 -s 1000000000000
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 9 -s off
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 9 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2000 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 9 -p ****
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 9 -s off
    
    </aside>
    
    <aside>
    💽 yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s on
    yarn storage-node leader:update-bag -i dynamic:channel:2330 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 0 -p ****
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 0 -s off
    
    </aside>