# Storage WG Status Report 11

3 June 2022 - 10 June 2022

**Storage Lead : *0x2bc***

# **Summary**

**GENERAL_WG_SCORE**

- Accounting of how much was spent on what.
    
    Totally during the period was spent ~4.5M tJOY
    
    - During the period ~4.5M tJOY was spent on salaries
    - 1.2M tJoy left on June 4, 2022
    - 11m tJoy was refilled
    - 7.5M tJoy is in the budget on Jun 11, 2022
    
    [Group budget](Storage%20WG%20Status%20Report%2011/Group%20budget%2046a79227632d4603b035ba47adb8f7ba.csv)
    

## **Actual hires made**

- Storage `Provider 10: sieemma` was hired.
- Two new Storage Provider vacancy were opened
    - One is open for everyone
    - Second one is open for `@bwhm`

## **Actual slashes imposed**

- No slashes

## **Actual firings done**

- No firings

## **Propose set of bounties that newcomers can tackle**

[New bounty for newcomers](Bounty%20For%20Newcomers%20eebfda64b726433f8fcd840ad3c115e4.md)

## **Changes made to the corresponding notion board.**

- No changes

## **A summary on how well the working group served it's intended purpose**

- One more week without incidents

Additional tasks:

- Deploy a Elastic Search server and have at least two SP nodes reporting to it
    
    <aside>
    💡 (1) Deploy a server to act as the endpoint
           [DONE](https://discord.com/channels/811216481340751934/812344681786507274/984437473184731146)
    (2) Have a storage node or two report to it, and compare the resource consumption before/after (a couple of times)
           -Have a storage node or two report to it - [DONE](https://discord.com/channels/811216481340751934/812344681786507274/984437473184731146) Actually more than 3 nodes are reporting to it. 
           - Compare the resource consumption before/after - the work in progress
    [](https://discord.com/channels/811216481340751934/812344681786507274/984437473184731146)(3) Make it public, so it can be used to debug and collect data
           DONE. See [https://kibana.joystreamstats.live/app/dashboards#/list](https://kibana.joystreamstats.live/app/dashboards#/list) 
                         (login:    joystream/ joystream)
    (4) Create a guide that explains how to set it up, and use it to look at the logs
           The work is in progress.
    (5) Use the most verbose log level, and IF that LOG_LEVEL differs from what was found in DEFAULT_LOGGING, outline what is added
            DONE. this crashes the node: 
            [https://github.com/Joystream/joystream/issues/3877](https://github.com/Joystream/joystream/issues/3877)
    
    </aside>
    
- Hire at least 1 more worker  ☑
    - the worker  @sieemma is hired
- Continue onboarding the new deputy  ☑
- Make at least one new bounty ☑
    - See [New bounty for newcomers](Bounty%20For%20Newcomers%20eebfda64b726433f8fcd840ad3c115e4.md)
- Increase the replication score  ☑
    - the rate is increaed from 4 to 6, you can check here [https://query.joystream.org/graphql](https://query.joystream.org/graphql)
- Create a opening without reward for @bwhm  ☑
    - the opening is created [https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14](https://dao.joystream.org/#/working-groups/openings/storageWorkingGroup-14)

## **Recommendations for what should be focused on in next council period in order to make group more effective**

- Make all reporting based on ES (elastic search)
- Configure more dashboards for ES
- Dig deeper into the failed upload objects issue

## **Suggested changes to the purpose or practices built in to this working group, other working groups, the council or Jsgenesis' role, in order to increase overall effectiveness of the group or the project**

- We can have periodic JSG meetings in order to get a better tech feedback

3 June 2022 - 10 June 2022

# Report

**REPORT_SCORE**

- How many storage buckets were created
    
    <aside>
    💽 Buckets at 3 June 2022:          10
    Buckets at 10 June 2022:        12
    
                                   Created:      2
    
    </aside>
    
- How many storage buckets were deleted
    
    <aside>
    💽
    
    Storage buckets deleted:         0
    
    </aside>
    
- How many bags were created.
    
    <aside>
    💽 Bags at 3 June 2022:          2626
    Bags at 10 June 2022:        2631
    
    Bags created: 2
    
    </aside>
    
- How many bags were deleted.
    
    <aside>
    💽 Bags deleted:  0
    
    </aside>
    
- What data objects were permanently lost, and if any, why.
    
    <aside>
    💽 Number of Objects Uploaded:	78
    Number of Objects Lost:	                 1
    % of failed uploads	                          1,2%
    
    </aside>
    
    [Permanently lost objects](Storage%20WG%20Status%20Report%2011/Permanently%20lost%20objects%20640ca679b47f42a085e9b2c129b3b621.csv)
    

<aside>
💽 We’ve lost 1 object with size of 0.01 MB

</aside>

- How many data objects were (attempted) uploaded, and
    - Number of data objects (attempted) uploaded
        
        <aside>
        💽 78
        
        </aside>
        
    - what was their total size,
        
        <aside>
        💽 5.3 GB
        
        </aside>
        
    - what was the size distribution.

![Untitled](../Archive/Storage%20WG%20Status%20Report%204/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%205/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%206/Untitled%201.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%207/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%208/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%209/Untitled.png)

![Untitled](../Archive/Storage%20WG%20Status%20Report%2011/Untitled.png)

- A chart (with raw data available for future use) that plots the changes in the values below over the council period, through snapshots at every 600 block:
    - data objects, number and size
    
    ![Untitled](../Archive/Storage%20WG%20Status%20Report%2011/Untitled%201.png)
    

![Untitled](../Archive/Storage%20WG%20Status%20Report%2011/Untitled%202.png)

- amount of bags;
    
    <aside>
    💽        Total amount of bags: 632
    
    </aside>
    

![Untitled](../Archive/Storage%20WG%20Status%20Report%2011/Untitled%203.png)

- (average) number and size of data objects in a bag

[(average) number and size of data objects in a bag](Storage%20WG%20Status%20Report%2011/(average)%20number%20and%20size%20of%20data%20objects%20in%20a%20bag%20f0229547eddd405c945f45fb3955c1ee.csv)

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
    10                        razumv                               TBD
    
    </aside>
    

- How much bandwidth did the individual nodes consume during the period.

 Every node transfers from 50 to 100 MB per day. As we use not really accurate measurement `ifconfig` tool, specific numbers per every node should not be used as a basis for decision marking.

![Untitled](../Archive/Storage%20WG%20Status%20Report%2011/Untitled%204.png)

- What, if anything, is the storage group doing the monitor the health of the system.
    
    <aside>
    💽 (1) On a daily basis: monitor status of the storage node [https://joystreamstats.live/storage](https://joystreamstats.live/storage) 
    (2) On a daily basis: check bug reports and complaints in the Discord to make sure there is no bugs related to download/upload
    
    </aside>
    
- A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.
    
          Shortly, what I did: 
          (1) hired one Storage Worker
          (2) created 2 new Storage Worker vacancies
          (3) created 2 new buckets for new Storage providers
          (4) increase replication rate 
     
    
    for i in $(seq 2567 2631) ; do
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 1 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 2 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 3 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 4 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 6 -p ****
    yarn storage-node leader:update-bag -i dynamic:channel:$i -k /root/.local/share/joystream-cli/accounts/SPLeader.json -a 8 -p ****
    done
    
    yarn joystream-cli working-groups:fillOpening --openingId 12 --applicationIds 27
    
    ./cli/bin/run working-groups:updateWorkerReward 9 4
    ./cli/bin/run working-groups:updateWorkerReward 10 4
    
    yarn storage-node leader:create-bucket -i 9 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -n 20000 -s 1500000000000
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 10 -s off
    
    yarn storage-node leader:create-bucket -i 10 -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -n 20000 -s 1500000000000
    yarn storage-node leader:update-bucket-status -k /root/.local/share/joystream-cli/accounts/SPLeader.json -p **** -i 11 -s off
    
    yarn joystream-cli working-groups:createOpening -g=storageProviders
    
    yarn joystream-cli working-groups:createOpening -g=storageProviders