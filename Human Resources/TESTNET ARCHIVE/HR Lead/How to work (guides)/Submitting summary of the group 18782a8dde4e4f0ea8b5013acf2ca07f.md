# Submitting summary of the group

---

## **Accounting**

![Untitled](Submitting%20summary%20of%20the%20group/Untitled.png)

### **Budget at the start of the term/Budget at the end of the term**

1. Use the [**guide](https://www.notion.so/How-to-find-the-start-and-end-block-of-the-council-term-cb6e33effa5a4b75b0ba8624cbd5e179?pvs=21)** to find the start block of the council term, the block hash with a block number.
2. Open this **[link](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate)**, specify the following data 
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%201.png)
    
3. Now you need to specify these numbers in Summary

### **Treasury refill**

1. Open Past Proposals Page - [https://dao.joystream.org/#/proposals/past](https://dao.joystream.org/#/proposals/past)
2. Specify the type - Update Working Group Budget and you need to find proposals that replenish the budget of the HR group.
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%202.png)
    
3. You can see in the proposals how much the group's budget was replenished. You need to find all the proposals for the period and calculate how much was replenished in total for the period.
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%203.png)
    

### **Lead rewards/Workers rewards**

1. Open graphql-console [https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql](https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql)
2. Enter this command
`query rewardPaidEvents { rewardPaidEvents (limit:1000000, where:{inBlock_gte:**2332800**,inBlock_lte: **2433600**, group: { name_eq: "operationsWorkingGroupBeta" }}) { amount }
}`
**In green I have highlighted the data that changes with each period - the start and end blocks of the period**
3. Next, you need to calculate the sum of all rewards
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%204.png)
    
4. I use Google tables for convenience.
Copy the data and paste it into a google table.
Divide the text into columns. Use space separation.
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%205.png)
    
5. At the bottom of the table, use the SUM command to calculate the total amount of rewards.
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%206.png)
    
6. Then you need to find one of the group leader's awards, copy the value and on the same page to find the number of payments to the leader with Ctrl + F.
260460*7=1823220 tJOY - **Lead rewards**
    
    ![Untitled](Submitting%20summary%20of%20the%20group/Untitled%207.png)
    
7. Subtract the group leader's rewards from the total.
10056650-1823220=8233430 tJOY - **Workers rewards**
8. Specify these values in Summary.

### **Discretionary spendings**

These are the group spending that the leader makes through polkadot extrinsics

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%208.png)

The first way to find this data is to look in the group's discord channel:

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%209.png)

The second way to find this data is to look in pioneer on the HR page of the group in the History section:

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2010.png)

You need to calculate all such spendings for the period and put them in the Summary.

## Group Changes

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2011.png)

**Hires/Slashes/Firings -** You need to specify who was fired/hired in the previous period

You can also watch this on the group's discord channel:

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2012.png)

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2013.png)

## Timesheet

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2014.png)

You need to ask the workers how much time they spent in the previous period.

**Example message:**
Hey
Please write me in the DM how many hours you have spent working in the past 7 days. I need this for reporting purposes. Deadline is tomorrow at 6:00 p.m. CET.
Please indicate only the time you spent at the screen.
Waiting time for newcomers in the chat room is also taken into account.
Be honest, please consider the pause.
When someone specifies 70 hours, it confuses other DAO members.
Thank you

## Bounties for newcomers

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2015.png)

Each period the group leader must come up with at least one new idea for a newcomer's Bounty.

## Notion Board Changes

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2016.png)

You need to specify what changes have been made in the Notion section of the HR group over the previous period.

## **List of completed tasks**

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2017.png)

You need to specify what tasks have been completed in the past period.

## **Ideas to improve your Working Group**

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2018.png)

You need to specify ideas for improving the HR group.

## **Ideas to improve other Working Group, Council, Jsgenesis**

![Untitled](Submitting%20summary%20of%20the%20group/Untitled%2019.png)

You need to specify ideas for improving other groups, Council, Jsgenesis.

---

**You need to post Summary on the forum in the HR Group category - [https://dao.joystream.org/#/forum/category/16](https://dao.joystream.org/#/forum/category/16)**
Example: [https://dao.joystream.org/#/forum/thread/778?post=1454](https://dao.joystream.org/#/forum/thread/778?post=1454)

**Working Group Summary Deadline: `B_n_el+10800 blocks`( election + 18h) for scoring period `n-1`**

---

## **Group Activity**

You also need to fill in the table with the activities of the workers of the working group - [Group Activity](../../Reports/Report%2010%2008%202022-18%2008%202022%20(Council%2019)/Group%20Activity%20b88467bd0c2a41b3a6aa2ae7170cede0.md) 

Each period has its own page with activities.