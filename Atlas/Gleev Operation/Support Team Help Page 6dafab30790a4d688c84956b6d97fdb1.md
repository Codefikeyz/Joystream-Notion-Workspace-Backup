# Support Team Help Page

# How to find Gleev Channel Id if we only know YouTube channel

1. Go to this tool 

[YouTube Channel ID - Find Channel ID, info & statistics](https://commentpicker.com/youtube-channel-id.php)

1. And enter the URL from YT to find the YT channel ID

![Screenshot 2023-10-23 at 13.48.34.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.48.34.png)

![Screenshot 2023-10-23 at 13.49.49.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.49.49.png)

3. Then copy this channel ID and search for it in Dynamo Backend using filter option (see below)
4. Once the record find, scroll the table to find the `Joystream channel ID` 

![Screenshot 2023-10-23 at 13.51.16.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.51.16.png)

1. Copy the ID to use it in other tools to find information about channel (like hubspot or postman)

![Screenshot 2023-10-23 at 13.53.42.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.53.42.png)

# How to check if the channel was paid the rewards?

1. First see if the channel was actually verified in Dynamo using filter options

![Screenshot 2023-10-23 at 13.56.07.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.56.07.png)

2. Then check *when* the channel signed up by checking `created at` field in Dynamo, and whether it was at least 1 Friday since.

![Screenshot 2023-10-23 at 13.56.39.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_13.56.39.png)

1. ⚠️if the channel signed up on Friday afternoon, it is likely that it did not make it to the calculations. To verify this, one needs to find it in the Hubspot database, using filter options:
    
    ![Screenshot 2023-10-23 at 14.29.17.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.29.17.png)
    

So we check the sign up reward in USD. Same applies for referral and sync rewards.. 
⚠️Remember that only videos longer than 5 minutes are rewarded. And maximum of 3 per week. 

![Screenshot 2023-10-23 at 14.29.28.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.29.28.png)

In this case we see that channel should have been paid as Sign up reward in USD set to 25

1. So now we need to check the transactions that were done for the channel reward account. 
To get the reward account we go to Postman and use channel id to find account address

⚠️ When using Orion requests for the first time during the day, do not forget to get the updated cookies form the Orion Auth endpoint (like for excluding channels) 

POST: [https://orion.gleev.xyz/api/v1/anonymous-auth](https://orion.gleev.xyz/api/v1/anonymous-auth)
Body of request: 

```
{
    "userId": "**********"
}
```

Instead of **** put the secret key for Orion

In the response choose `cookies` And copy the `value`  (in the example below its `8%2bs..`). You will need it to use it in the header for other requests to check data from Orion.

![Screenshot 2023-10-23 at 14.35.10.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.35.10.png)

Then make the actual request to check reward account for channel

POST: [https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)
Header: make sure to add session_id (from the Auth cookies response as explained above)

![Screenshot 2023-10-23 at 14.41.16.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.41.16.png)

Body of request: 

```
{
  channels(where: {id_eq: "29948"}) {
    id
    rewardAccount
    ownerMember {
      handle
      controllerAccount
    }
  }
}
```

Check response:

```
{
    "data": {
        "channels": [
            {
                "id": "29948",
                "rewardAccount": "j4To6jgKfy8MgiMRDXzc15ggN8AnFC1UKcGukNkGY4WbH3QXs",
                "ownerMember": {
                    "handle": "cryptolive8887",
                    "controllerAccount": "j4RbmiJsXrWHgQ5rqCY9eGfWdSVc1n4jg15t8xnbU2fYD5RoM"
                }
            }
        ]
    }
}5
```

1. Now we have the channel rewardAccount `j4To6jgKfy8MgiMRDXzc15ggN8AnFC1UKcGukNkGY4WbH3QXs`

We will check all transactions for this account on SubScan:

[Subscan | Aggregate Substrate ecological network high-precision Web3 explorer](https://joystream.subscan.io/)

Enter the address to search and click “Search”

![Screenshot 2023-10-23 at 14.43.36.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.43.36.png)

In the results there will be option to check all balance transfers

![Screenshot 2023-10-23 at 14.44.15.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.44.15.png)

As we can see there were no transfers to this account (and Balance history tab is also empty). 

That means that channel was not paid, even tho it should have been. In this case you tag myself and `@Zeeshanakram` in the `youtube-sync` channel on Discord, like so 
(just add cc @dmtrmltsv):

![Screenshot 2023-10-23 at 14.48.38.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.48.38.png)

# Cannot sign up - `channel already exists` but its not in Dynamo channels.

Sometimes people have problems signing in to their account (`channel already signed up error`) but you cannot find it in the database for channels on Dynamo. That means that their registration was interrupted, they created a user record but channel did not get created.. 

In order to resolve this we need to ask Zeeshan to remove the user from the database (but first check if that record is really there)

1. Go to dynamo and check for channels registered with email using filters: 

![Screenshot 2023-10-23 at 14.55.17.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.55.17.png)

Here there are no channels so let’s check users

2.  Check users table in Dynamo for such email (see radio button on the left “users”), thats how to change tables

![Screenshot 2023-10-23 at 14.56.05.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.56.05.png)

3. Ask Zeeshan to remove the record using `joystreamMemberId` or email address like so:

![Screenshot 2023-10-23 at 14.57.48.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_14.57.48.png)

1. Once confirmed, go back to reporter and ask to try and sign up again from [Gleev.xyz](http://Gleev.xyz)/ypp  

# The bonus did not arrive to my account

They will also attach a screenshot of the dashboard.

![Screenshot 2023-10-23 at 16.40.34.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_16.40.34.png)

What that means is that they do not understand (a lot of users actually also) that there are separate wallets for Channel and Member.  

👉🏻 In this case ask them to check their payments dashboard>   [gleev.xyz/studio/payments](https://gleev.xyz/studio/payments) and most likely the payment will be there on the channel. 

# Withdrawal failed

Withdrawals is a two-step transaction 

1. From Channel wallet to Membership wallet
2. From Membership wallet to External account (Exchange)

If people had errors, you can check their reward wallet transactions and confirm it was successful on Subscan. Then advise them like so:

    
    ![Screenshot 2023-10-23 at 17.48.54.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_17.48.54.png)
    
    ![Screenshot 2023-10-23 at 17.45.57.png](Support%20Team%20Help%20Page/Screenshot_2023-10-23_at_17.45.57.png)
    
    ## QN Switchover
    
    joystream-cli api:setUri wss://rpc.joyutils.org
    joystream-cli api:setQueryNodeEndpoint [https://query.joyutils.org/graphql](https://query.joyutils.org/graphql)