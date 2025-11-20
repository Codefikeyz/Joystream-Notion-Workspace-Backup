# Payouts (Calculation & Execution)

## Intro

This page covers the sequence of steps required to perform weekly payouts for YPP program. 

NB: the payouts are done every Tuesday AM CET time. The period of payout calculation covers all channels who signed up from Monday 12 CET (midday) previous week to Monday 12 CET current week Monday. So the cutoff point is always yesterday 12 CET.

Some of the channels which signed up may not be included into the payments due to the backlog of verifications. The payments are calculated **only** for the channels that are contained in Hubspot - [YPP Criustomers list](https://app-eu1.hubspot.com/contacts/139496108/objects/0-1/views/22323715/list).  Channels records, with respective YPP verification status get synced to Hubspot via cron job. 

⚠️ At the time of writing the cron job is disabled due to large number of records, so the sync needs to be pushed manually.
⚠️ In the video that I recorded I already have the CLI installed and up to date with the right version 
⚠️ In the video that I recorded I already have the payment account set up

## Payout CLI commands

### Set up CLI (for Both Calculation & Payouts)

You only need to do these steps once - to set up the CLI

1. Run `npm install -g @joystream/cli@1.2.0`
2. Run `git clone -b ypp_ops_scripts  --single-branch https://github.com/zeeshanakram3/youtube-synch.git youtube-synch-ops`
3. Run `cd youtube-synch-ops/ypp-operations`
4. Run `npm install`

### Pull fresh CLI update

⚠️ This may be required time to time after the update to the logic of payouts. Not required for initial set up.

Go to the folder of `youtube-synch-ops/ypp-operations` and run `git pull`

In the terminal it may look like this:

```
dm@Dmitrys-MacBook-Pro ~ % cd desktop
dm@Dmitrys-MacBook-Pro desktop % cd joystream
dm@Dmitrys-MacBook-Pro joystream % cd youtube-synch-ops/ypp-operations
dm@Dmitrys-MacBook-Pro youtube-synch-ops % **git pull**
remote: Enumerating objects: 295, done.
remote: Counting objects: 100% (295/295), done.
remote: Compressing objects: 100% (110/110), done.
remote: Total 295 (delta 198), reused 270 (delta 178), pack-reused 0
Receiving objects: 100% (295/295), 69.36 KiB | 550.00 KiB/s, done.
Resolving deltas: 100% (198/198), completed with 46 local objects.
From <https://github.com/zeeshanakram3/youtube-synch>
   ad66775..5d0e2f1  ypp_ops_scripts       -> origin/ypp_ops_scripts
   7e7d9f0..ebb4425  dev                   -> origin/dev
   96a3891..5eb03e6  main                  -> origin/main
 * [new branch]      post_ypp2_fixes_and_feats -> origin/post_ypp2_fixes_and_feats
 * [new branch]      ypp_sync_improvements -> origin/ypp_sync_improvements
 * [new branch]      ypp_top_referrers_endpoint -> origin/ypp_top_referrers_endpoint
Updating ad66775..5d0e2f1
Fast-forward
 CHANGELOG.md                                       |  20 ++
 package.json                                       |   4 +-
 src/app/index.ts                                   |   1 -
 .../sync/addUnauthorizedChannelForSyncing.ts       |   1 -
 src/repository/DynamodbService.ts                  |  12 +-
 src/repository/channel.ts                          |  96 +++++++--
 src/repository/video.ts                            |  14 +-
 src/services/httpApi/api-spec.json                 | 114 +++++++---
 src/services/httpApi/controllers/channels.ts       |  10 +-
 src/services/httpApi/controllers/referrers.ts      |  32 +++
 src/services/httpApi/dtos.ts                       |  68 ++++--
 src/services/httpApi/main.ts                       |   5 +-
 src/services/runtime/client.ts                     |  10 +-
 src/services/storage-node/api.ts                   |   6 +-
 .../syncProcessing/ContentCreationService.ts       |  28 ++-
 .../syncProcessing/ContentDownloadService.ts       |  24 +--
 src/services/syncProcessing/PriorityQueue.ts       | 101 ++++++---
 .../syncProcessing/YoutubePollingService.ts        |   2 +-
 src/services/syncProcessing/index.ts               |  39 ++--
 src/services/youtube/api.ts                        |   3 +-
 src/types/youtube.ts                               |  28 ++-
 src/utils/misc.ts                                  |   2 +
 yarn.lock                                          |  30 +--
 ypp-operations/README.md                           |  12 ++
 ypp-operations/patches/@joystream+cli+1.2.0.patch  |  61 +++---
 ypp-operations/scripts/calculateYppRewards.ts      |   3 +
 ypp-operations/scripts/updateHubspotContacts.ts    |   3 +
 ypp-operations/src/cli/base/default.ts             |   5 +-
 ypp-operations/src/cli/base/joystreamCli.ts        |  94 ++++----
 ypp-operations/src/cli/commands/payRewards.ts      |  59 +-----
 ypp-operations/src/config.ts                       |  27 +--
 ypp-operations/src/dynamodb.ts                     |  70 +++---
 ypp-operations/src/hubspot.ts                      | 160 +++++++-------
 ypp-operations/src/index.ts                        |  10 +-
 ypp-operations/src/recheckVideoState.ts            | 236 +++++++++++++++++----
 ypp-operations/src/types.ts                        | 156 ++++++++++++--
 36 files changed, 1040 insertions(+), 506 deletions(-)
 create mode 100644 src/services/httpApi/controllers/referrers.ts
 create mode 100644 src/utils/misc.ts
 create mode 100644 ypp-operations/scripts/calculateYppRewards.ts
 create mode 100644 ypp-operations/scripts/updateHubspotContacts.ts
dm@Dmitrys-MacBook-Pro youtube-synch-ops %

```

### Declare payment account

<aside>
💡 
We are executing payments from `member id 5456`

First time one need to import account associated with membership use this command before making member remark

</aside>

![Screenshot 2023-11-26 at 12.47.45.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-26_at_12.47.45.png)

### Connect to the right endpoints

Make sure you are connected to the production endpoints for QN and RPC nodes before trying to run payment commands

**Prod**

```jsx
api:setQueryNodeEndpoint <https://query.joystream.org/graphql>
api:setUri <wss://rpc.joystream.org:9944/>
```

DEV

```jsx
api:setQueryNodeEndpoint <[https://18.195.31.204.nip.io/query-node/server/graphql](https://18.195.31.204.nip.io/query-node/server/graphql)>
api:setUri <wss://18.195.31.204.nip.io/ws-rpc>
```

### Commands to run on the day of payout

You need to do the following commands once per terminal session (i.e. if you close the terminal window then do it again)

You would need Hubspot API Key  for it, and here’s how to get it:

![Screenshot 2023-11-21 at 14.32.42.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_14.32.42.png)

1. **Run `export [HUBSPOT_API_KEY](https://explorer.walletconnect.com/onekey)=YOUR_HUBSPOT_KEY`**
2. **Run payRewards**

There are two specific cli commands in for executing the payouts, one for doing payouts per channel bases while other for doing payouts in batch (to all the channel that are owed some reward)

- [payRewardForChannel](https://github.com/zeeshanakram3/youtube-synch/blob/ypp_ops_scripts/ypp-operations/docs/cli/payRewardForChannel.md)
- [payRewards](https://github.com/zeeshanakram3/youtube-synch/blob/ypp_ops_scripts/ypp-operations/docs/cli/payRewards.md)

Example of executing `payRewardForChannel` to pay a single channel

```jsx
./bin/run payRewardForChannel --channelId 26503 --joyPrice 0.0022 --rationale "YPP Rewards Date From Date To" --payerMemberId 5456
```

Example of executing  `payRewards`for multiple channels at once (in batch). 
The batch limit on the chain is 100 channels. I use 90 max.
 

```jsx
./bin/run payRewards --joyPrice 0.053176 --rationale "YPP Rewards 14.11 - 21.11" --payerMemberId 5456 --batchSize 90
```

## Process of payment - step by step

### **1. Update Hubspot with fresh status from Dynamo**

Ensure up to date statuses for channels are synced to Hubspot from Dynamo. Ask @Zeeshan on Discord to push the fresh update.

![Screenshot 2023-11-21 at 13.45.06.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_13.45.06.png)

### **2. Confirm update succeeded**

Perform visual check of [channels in Hubspot](https://app-eu1.hubspot.com/contacts/139496108/objects/0-1/views/22323715/list). The total number of channels in the list should increment after the fresh push, and the records for “date of sign up to YPP” should get refreshed.

*Before*

![Screenshot 2023-11-21 at 13.39.29.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_13.39.29.png)

*After*

![Screenshot 2023-11-21 at 13.55.01.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_13.55.01.png)

The records got updated so we can progress to calc script..

### **3. Run the calculation script**

Run the calculation script for sign up, referral and sync rewards. Ask @Zeeshan on Discord to run the calc script. 

If you want to run the run the calculation script yourself do the following steps.

***Run terminal:***

1. `cd youtube-sync-ops`
2. `cd ypp-operations` → get to respective folder
3. `nano .env`

Enter the following configuration/environment variables required by the calculation script 

```jsx
AWS_ACCESS_KEY_ID=*******
AWS_SECRET_ACCESS_KEY=*******
AWS_REGION=eu-central-1
HUBSPOT_API_KEY=*******
```

You can get `HUBSPOT_API_KEY` from the Hubspot settings page as described in the above section.

For getting `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`, you need to contact @**mokhtarnaamani** on Discord. He will create role specific key for you to access DynamoDB tables, which the calculation script will use to calculate rewards.

Also, important to note that step 3 is only needed once.

1. `npx ts-node scripts/calculateYppRewards.ts` This will calculate the rewards and update the Hubspot will calculated rewards for each channel

### **4. Confirm script updates**

****I usually just sort asc/ desc the channels by the table columns listed below and cross-check with their date of sign up to the program. 

`Latest date checked` - this field gets updated with the timestamp of last calc script executed
`New synced vids` - will be added for the period of script - total count
`Videos sync reward in USD` - limited to max 3 videos of duration > 5 minutes and based on channel tier
`Sign up rewards in USD` - sign up reward based on channel tier
`Latest referral reward in USD` - referral reward based on the tier of channels referred
`Latest YPP reward status` - will need to be “to pay” - this is the key field that payout script is using to include channels to the payment. 

⚠️ After running the calculation script and before running the payout script any manual updates to the amounts to be paid can be done.

Before the calc script:
****

![Screenshot 2023-11-21 at 13.51.22.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_13.51.22.png)

After the calc script:

![Screenshot 2023-11-21 at 20.00.56.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_20.00.56.png)

### **5. Execute payment  + Video**

****⚠️ For payment we are using the yt-sync scripts. I have already pre-set up. See [this section](Payouts%20(Calculation%20&%20Execution)%207cdfcb129b6e4ea3b915c07bb8f67c78.md) for how to.
****⚠️ Check JOY price on any exchange, I use [MEXC.](https://www.mexc.com/exchange/JOYSTREAM_USDT?_from=search) 

Run terminal:
cd desktop *(this folder will be specific to you)* 

cd joystream *(this folder will be specific to you)*

`cd youtube-sync-ops`

`cd ypp-operations` → get to respective folder
`export HUBSPOT_API_KEY=pat-eu1-*************-*********a19e` hit enter →  no response means all okay
`./bin/run payRewards --joyPrice 0.053176 --rationale "YPP Rewards 14.11 - 21.11" 
--payerMemberId 5456 --batchSize 90` →  “Do you want to pay N channels?” 
⚠️ Make sure that you have “ ” signs edited exactly as they are in the terminal itself as editing the above string in text editors may change the quotes to the unsupported format!

hit `Y` and hit enter → “Enter your account Password” 
`type in password for paying member controller acc` and hit enter → It will connect to runtime and query nodes and execute batch payment (for as many channels as there are in the batch), then ask you to type in password again. 
`Type password and hit enter` → Repeat as many times as needed before you see this message: `Successfully paid rewards to YPP channels!`

**Here’s the link to the video recording of payouts execution
<redacted>**

**Here’s how it looks in the terminal**

<redacted video>

![Screenshot 2023-11-21 at 15.27.11.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_15.27.11.png)

![Screenshot 2023-11-21 at 15.26.20.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_15.26.20.png)

![Screenshot 2023-11-21 at 15.26.28.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_15.26.28.png)

### 6**. Confirm payment succeeded in Hubspot**

For all channels which had any rewards, we have 3 fields updated

`Latest YPP reward status` - must be set to “paid” to all channels whose rewards are >0 for the last period.
`Latest Overall YPP Reward in JOY` - must be populated with the amount based on JOY/ USDT ER
`Total Rewards in JOY` - must not be empty for the newly signed up channels

`Latest YPP reward status`  - must be “**paid**”

![Screenshot 2023-11-21 at 20.01.46.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_20.01.46.png)

### 7. Export Hubspot Data for Reporting

All stats are posted to [this page.](../YouTube%20Partner%20Program%20Outline/YouTube%20Creator%20Payouts%2002f7cf50972145bfb64c8543914ae4bb.md)

Using the export from Hubspot as a csv / xls I put together the total stats based on the columns present in the spreadsheet. 

First export the records

![Screenshot 2023-11-21 at 19.24.43.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.24.43.png)

Once the export file is ready, it can be downloaded. The notification comes via email and as an in-app toaster message.

For the total verified channels count I use Hubspot filters as so

`Lifecycle stage` = Customer
`Lead status` = Connected

![Screenshot 2023-11-21 at 19.25.52.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.25.52.png)

For the total count of referrers, who did not become part of YPP I use the following filters:

`Lifecycle stage` = Customer
`Lead status` = Referrer

### 8. Send out comms on Discord

Once the payment is done and the stats are ready, I post the update to the `creators` channel on Discord. But also duplicate to `creator-support` This helps to reference this post by support team for creators who reach out with questions about their payment. 

Links to channels:

[Discord - A New Way to Chat with Friends & Communities](https://discord.com/channels/811216481340751934/812344859921743872)

[Discord - A New Way to Chat with Friends & Communities](https://discord.com/channels/811216481340751934/1053294778529353788)

### 9. Send out comms via Hubspot

I echo the message sent on Discord in the email, sent from Hubspot as well.  

1. Go to marketing tab and **select email**
. 

![Screenshot 2023-11-21 at 19.36.06.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.36.06.png)

2. Click on **Create Email**

![Screenshot 2023-11-21 at 19.36.16.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.36.16.png)

3. Choose **Regular**

![Screenshot 2023-11-21 at 19.36.20.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.36.20.png)

4. Select **Simple**

![Screenshot 2023-11-21 at 19.36.24.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.36.24.png)

5. In the **Edit tab** type up email (or clone and edit)

![Screenshot 2023-11-21 at 19.40.38.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.40.38.png)

1. On the **Settings tab** select `ypp@gleev.xyz` for the *from* address, add subject and preview text

![Screenshot 2023-11-21 at 19.41.26.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.41.26.png)

1. On the **Send or schedule** tab choose `YPP Verified` list of recepients 

⚠️ **NB:** All new verified channels are added to Hubspot as ***marketing contacts.***  Marketing contacts count is the basis of Hubspot billing on our plan, so it rises dramatically. A more cost-effective and time consuming alternative would be to export the list of recepients and import to Sendgrid. And send the emails from Sendgrid. The gleev@xyz needs to be configured there to enable it. 

    
    ![Screenshot 2023-11-21 at 19.41.38.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.41.38.png)
    

8. Automation is not involved, so all we need to do now is to review and send email. Voila.  

![Screenshot 2023-11-21 at 19.42.30.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.42.30.png)

### 10. Handle support

Support comes in three places

1. [Creator-support channel](https://discord.com/channels/811216481340751934/1053294778529353788) on Discord
2. Email responses to weekly payout emails
3. Usersnap support issues to Github [new issues pipeline of this view.](https://github.com/Joystream/atlas#workspaces/atlas-600edbb8799cc700103bc2d7/board?repos=315632044)  

For point 3 - I assign most of non-critical issues not connected to failed payments to Richard (github handle `rchrdcstro`) and move them to support pipeline as shown in the picture below.

![Screenshot 2023-11-21 at 19.54.13.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.54.13.png)

![Screenshot 2023-11-21 at 19.55.33.png](Payouts%20(Calculation%20&%20Execution)/Screenshot_2023-11-21_at_19.55.33.png)