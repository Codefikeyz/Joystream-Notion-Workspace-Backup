# Gleev Operation

# Content Moderation

## Exclude channel/video/objectId from Gleev

1. Find video URL you want to block e.g. [https://gleev.xyz/video/28](https://gleev.xyz/video/28)
2. Get videoID from the URL, here its 28.
3. Go to App Repo [https://github.com/Joystream/gleev](https://github.com/Joystream/gleev)
4. Go to main> packages> atlas.config.yml [https://github.com/Joystream/gleev/blob/main/packages/atlas/atlas.config.yml](https://github.com/Joystream/gleev/blob/main/packages/atlas/atlas.config.yml)
5. Find the code with content blocking and add video ID to the list
    
    ![Screenshot 2023-01-23 at 14.56.57.png](Gleev%20Operation/Screenshot_2023-01-23_at_14.56.57.png)
    

**To block Thumbnails and MediaMeta for this video**

1. Go to graphql interface [https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)
2. Find the video Data Objects using this query:

`query {
videoByUniqueInput (where:{
id:"294"
}) {
id
thumbnailPhotoId
mediaMetadataId}
}`
3. Get Data object IDs from query output (right hand side)

    
    ![Screenshot 2023-01-23 at 14.58.18.png](Gleev%20Operation/Screenshot_2023-01-23_at_14.58.18.png)
    
4. Add the data objects ID to the config:

    
    ![Screenshot 2023-01-23 at 14.58.51.png](Gleev%20Operation/Screenshot_2023-01-23_at_14.58.51.png)
    
5. Deploy changes to master/ main branch

    
    ![Screenshot 2023-01-23 at 14.59.21.png](Gleev%20Operation/Screenshot_2023-01-23_at_14.59.21.png)
    
6. After checks are completed, the app version with the blocked content will be deployed. Usually takes 3-4 minutes or less. 
    
    ![Screenshot 2023-01-23 at 14.59.35.png](Gleev%20Operation/Screenshot_2023-01-23_at_14.59.35.png)
    
7. Check if the video/ channel/ object ID is blocked: 

    
    ![Screenshot 2023-01-23 at 15.16.17.png](Gleev%20Operation/Screenshot_2023-01-23_at_15.16.17.png)
    
    ![Screenshot 2023-01-23 at 16.19.46.png](Gleev%20Operation/Screenshot_2023-01-23_at_16.19.46.png)
    
    ### 
    

## Check reported videos

There’s a feature for the users and content curators to report content for subsequent curation. This is done via the Report Feature, available from the overflow menu on the video details page: 

![Screenshot 2023-01-23 at 15.21.57.png](Gleev%20Operation/Screenshot_2023-01-23_at_15.21.57.png)

To access the list of the reported videos..

1. Go to [https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)

2. Run query

`query {
reportedVideos {
id
videoId
}`

3. To succeed you need to authorise using password. Open playground, and in the bottom there is http headers section, where you need to post the password together with your query

`{
  "Authorization": "yourpassword"
}`

# Ypp Operations

## Direct member payments to channels

In order for the GW operator to pay channel directly, a member payment remark can be used. It can be executed via CLI.  Below are the example of commands to make the payment and attribute it to channel (1), or a specific video (2). 

When the payment is made, by default CLI will prompt to choose the *membership* from which the payment must be made, or it can be specified with a special param `--useMemberId ***`, like it is shown in example (1) 

NB:The payment is made from the member’s *controller account*.

Example CLI commands for payments: 

1. `joystream-cli content:directChannelPayment --rationale "abcd" --channelId 1 --amount 10 --useMemberId 133`
NB: (default `payment_context` is assumed to be channel)
2. `joystream-cli content:directChannelPayment --rationale "sign up reward " --channelId 1 --amount 10 --videoId 1` 
NB: (payment_context is video 1)

Or if you are in the CLI folder already go for:
`./bin/run content:directChannelPayment --rationale "Payouts Testing on Prod" --channelId 25829 --amount 10000000000 --useMemberId` 5456

`./bin/run content:directChannelPayment --rationale "Sign up bonus June 16th" --channelId 26372 --amount 50000000000000 --useMemberId` 5456

To import account associated with membership use this command before making member remark:

    
    ![Screenshot 2023-03-13 at 18.18.41.png](Gleev%20Operation/Screenshot_2023-03-13_at_18.18.41.png)
    

## YPP payout script via CLI

Open terminal and start running the following commands

1. Run `git clone https://github.com/zeeshanakram3/youtube-synch.git`
2. Run `git checkout ypp_ops_scripts`
3. Run `cd ypp-operations`
4. Run `yarn`
5. Run `export HUBSPOT_API_KEY=YOUR_HUBSPOT_KEY`

Ideally you only need to do these steps once per terminal session (i.e. if you close the terminal window then do it again)

There are two specific cli commands in for executing the payouts, one for doing payouts per channel bases while other for doing payouts in batch (to all the channel that are owed some reward)

1. [payRewardForChannel](https://github.com/zeeshanakram3/youtube-synch/blob/ypp_ops_scripts/ypp-operations/docs/cli/payRewardForChannel.md)
2. [payRewards](https://github.com/zeeshanakram3/youtube-synch/blob/ypp_ops_scripts/ypp-operations/docs/cli/payRewards.md)

However, initailly I would advise to use command for doing payouts per channel base (i.e. use `payRewardForChannel`) and 1. before confirming action the action ensure that reward is correct, 2. after executing the command ensure that hubspot entry has been updated i.e. the contact status changed to `Paid` etc This could help in identifying any errors in the payout command logic & could save us from any major loss

Example of executing `payRewardForChannel` and  `payReward`s

```
./bin/run payRewardForChannel --channelId 26503 --joyPrice 0.0022 --rationale "" --payerMemberId 20

```

```
./bin/run payRewards --joyPrice 0.0022 --rationale "" --payerMemberId 5456 --batchSize [size]
```

To get the list of all channels that are owed some rewards you can execute `getRewardsOwed` command as

```
./bin/run getRewardsOwed --joyPrice 0.0022

```

It will output the results on console as

![](https://user-images.githubusercontent.com/37098720/252560908-36b5eb94-2fff-4559-8baf-e08ced824fa2.png)

## Checking Stats

### `youtube-synch stats`

Returns channels created from date x till date y + link to joystream and youtube channel + Referrer ids.

- [`youtube-synch stats:channels`](https://github.com/Joystream/youtube-synch/blob/2c59b96145ab4903ce078b9180cba2b1c1de1b5c/src/cli/docs/stats.md#youtube-synch-statschannels)
- [`youtube-synch stats:videosByChannel`](https://github.com/Joystream/youtube-synch/blob/2c59b96145ab4903ce078b9180cba2b1c1de1b5c/src/cli/docs/stats.md#youtube-synch-statsvideosbychannel)

### `youtube-synch stats:channels`

Returns channels created from date x till date y + link to joystream and youtube channel + Referrer ids.

`USAGE
$ youtube-synch stats:channels

OPTIONS
  -c, --configPath=configPath  [default: ./config.yml] Path to config JSON/YAML file (relative to current working
                               directory)

  -d, --appDomain=appDomain    Domain of the application that should be used to construct the channel URLs

  -y, --yes                    Answer "yes" to any prompt, skipping any manual confirmations

  --httpApiUrl=httpApiUrl      [default: http://localhost:3001] HttpApi URL from where channels & videos stats should be
                               fetched`

Example for gleev.prod

.`/bin/run stats:channels --httpApiUrl` [https://18.197.227.145.nip.io/](https://18.197.227.145.nip.io/)

### `youtube-synch stats:videosByChannel`

Returns the number of videos created (for a given channel) from date x till date y + link to joystream and youtube channel + Referrer ids.

`USAGE
  $ youtube-synch stats:videosByChannel

OPTIONS
  -c, --configPath=configPath              [default: ./config.yml] Path to config JSON/YAML file (relative to current
                                           working directory)

  -d, --appDomain=appDomain                Domain of the application that should be used to construct the channel &
                                           videos URLs

  -y, --yes                                Answer "yes" to any prompt, skipping any manual confirmations

  --httpApiUrl=httpApiUrl                  [default: http://localhost:3001] HttpApi URL from where channels & videos
                                           stats should be fetched

  --joystreamChannelId=joystreamChannelId  (required) ID of the synced Joystream channel for which the uploaded videos
                                           stats should be returned`

## Whitelist channel

- `POST /channels/whitelist` to whitelist a channel
- `DELETE /channels/whitelist/{ytChannelHandle}` to remove a whitelisted channel

And use the below in the body (Youtube Channel handle)

[
{"channelHandle": "@testchannel8581"}
]

# DAO Operations

## Check Content WG payments

[https://query.joystream.org/graphql](https://query.joystream.org/graphql)

```jsx
query budgetSpendingEvents {
budgetSpendingEvents (limit: 30000, where:{group:{id_eq:"contentWorkingGroup"}}) {
id
groupId
reciever
amount
rationale
}
}

```

## Make Payout Proposal Payment

1. **Compose the payload Vector file, specifying the payouts to individual channels in the JSON format.** 

[Payout_Proposal_Example.JSON](Gleev%20Operation/Payout_Proposal_Example.json)

****Sample Abstract:

```json
[
{
"channelId": 40,
"cumulativeRewardEarned": "50000000000000",
"reason": "Reward for most views"
},
{
"channelId": 9,
"cumulativeRewardEarned": "10000000000000",
"reason": "Reward for longest comments thread"
},
]
```

**Parameters**
a. Channel ID -  can be found in the URL 

![Screenshot 2023-01-26 at 14.12.22.png](Gleev%20Operation/Screenshot_2023-01-26_at_14.12.22.png)

b. cumulativeRewardEarned - the total amount awarded/ earned by channel. 

⚠️ For subsequent payments to the same channel, the value of the reward has to include the previous payment. Meaning: if channel 1 was paid 4k JOY in period1, and needs to be paid 2K JOY more in period2, the value that needs to be put to cumulativeRewardEarned must be 6k
⚠️ The value is specified in HAPI, the base denomination of JOY. 1 JOY = 10000000000 HAPI. Use this tool for simplicity of conversion: [https://joyutils.org/](https://joyutils.org/)
⚠️ The `cumulativeRewardEarned` must be higher than `cumulativeRewardClaimed`  for the channel to be able to claim rewards. 

The way to check the cumulativeRewardClaimed for the channel is using Graph QL interface: [https://atlas-next.joystream.org/query-node/server/graphql](https://atlas-next.joystream.org/query-node/server/graphql)

```jsx
query {
channelByUniqueInput(where: {id: "39"}) {
id
cumulativeRewardClaimed
}
}
```

c. Reason - is a text field. 

1. **Prepare the Payload Binary File**
From the Joystream mono repo (on the `ephesus` branch) run the following CLI command and note the `COMMITMENT`
    
    ```
    cli/bin/run content:generateChannelPayoutsPayload -i path/to/ChannelPayoutsVector.json -o payload.bin
    
    ```
    
2. **Create the Payout Proposal on Pioneer uploading the *Binary file* to the proposal specific parameters**
NB: ⚠️ as part of this proposal `minimumClaimableAmount` and `maximumClaimableAmount` are defined in JOY tokens. For the channel to be able to claim JOY tokens, their totalEarnedRewards-totalClaimedRewards needs to fall within the limits defined in this proposal.
3. **Vote on proposal to execute**
4. **Get the Payload Data Object ID for the storage system**
This can be viewed on the proposal preview page after execution or lternatively, once the proposal is executed the `DATA_OBJECT_ID` can be queried on [https://atlas-next.joystream.org/query-node/server/graphql](https://atlas-next.joystream.org/query-node/server/graphql) using the `COMMITMENT` from step 2. See screenshot and query below:
    
    ![Screenshot 2023-02-09 at 11.59.30.png](Gleev%20Operation/Screenshot_2023-02-09_at_11.59.30.png)
    
    ```
    
    {
      channelPayoutsUpdatedEvents (where: { commitment_eq: "COMMITMENT" }) {
        payloadDataObjectId
      }
    }
    
    ```
    
5. **Create the json file to upload the binary to the storage system**
Create a json file (lets call it `upload.json`):
    
    ```
    {
      "bagId": "static:council",
      "assets": [ { "objectId": "DATA_OBJECT_ID", "path": "path/to/payload.bin" } ]
    }
    
    ```
    
6. **Upload the payload using the json, by running:**
    
    ```
    cli/bin/run content:reuploadAssets -i upload.json
    
    ```
    

1. **Channels can now claim their payouts via Payment dashboard available in the Studio view**

[https://atlas-git-ypp-joystream.vercel.app/studio/payments](https://atlas-git-ypp-joystream.vercel.app/studio/payments)

Claimable rewards widget view, when no rewards were allocated to the channel via Council Payouts. 
    
    ![Screenshot 2023-01-26 at 14.39.59.png](Gleev%20Operation/Screenshot_2023-01-26_at_14.39.59.png)
    

When rewards payload is uploaded to storage system the amount `cumulativeRewardEarned` - `cumulativeRewardClaimed`  is displayed in the “Claimable rewards” widget.

![Screenshot 2023-01-26 at 14.38.37.png](Gleev%20Operation/Screenshot_2023-01-26_at_14.38.37.png)

Claim Payout Modal - channels can only claim full amounts, and unable to specify how much to claim. Rationale is not displayed to the channels. 

![Screenshot 2023-01-26 at 14.38.52.png](Gleev%20Operation/Screenshot_2023-01-26_at_14.38.52.png)

⚠️Only Claimed Rewards are displayed in the Payments history table. The awarded rewards and rationale is not displayed to the channels. 

# Useful CLI commands

Update version of CLI

Open YT-synch directory in terminal
- Do

```
git checkout main
```

-

```
git remote update
```

-

```
git merge upstream/main
```

1. git clone [https://github.com/Joystream/youtube-synch.git](https://github.com/Joystream/youtube-synch.git)

1. cd youtube-synch
2. yarn install
3. Update CLI endpoints
4. api:setQueryNodeEndpoint [https://query.joystream.org/graphql](https://query.joystream.org/graphql)

__

[Channel Verification](Gleev%20Operation/Channel%20Verification%205bb62120149348beb8f398c592e73ce1.md)

[Verified Notifications mgt](Gleev%20Operation/Verified%20Notifications%20mgt%20d2b2dfccb1334d08b02bb46980cf2545.md)

[Messaging Templates](Gleev%20Operation/Messaging%20Templates%20acaf7ee5239b48748748f0fbdb449ea7.md)

[Homepage Feed Management](Gleev%20Operation/Homepage%20Feed%20Management%2026cd9aaae43f4a6ca49af06da4bb0a88.md)

[Support Team Help Page](Gleev%20Operation/Support%20Team%20Help%20Page%206dafab30790a4d688c84956b6d97fdb1.md)

[Payouts (Calculation & Execution)](Gleev%20Operation/Payouts%20(Calculation%20&%20Execution)%207cdfcb129b6e4ea3b915c07bb8f67c78.md)

[Product and Ops Tools](Gleev%20Operation/Product%20and%20Ops%20Tools%2011c391579e7540c684d0b07c85a11140.md)

[Backing up Orion database](Gleev%20Operation/Backing%20up%20Orion%20database%20775d36e8815d414ab1b3c246c26d155b.md)

[Featuring CRTs](Gleev%20Operation/Featuring%20CRTs%20b1141701e34d4c089ce41f4d773528bd.md)

[Managing Video Category Heros](Gleev%20Operation/Managing%20Video%20Category%20Heros%205c0ad17e600344bfb96f26043a2ca8a5.md)

[Managing Featured Carousel](Gleev%20Operation/Managing%20Featured%20Carousel%20b417e23267ee4d3f875f6e4f56044106.md)

[Archived](Gleev%20Operation/Archived%20f98c48dcef634e43aaa80adc246473b4.md)