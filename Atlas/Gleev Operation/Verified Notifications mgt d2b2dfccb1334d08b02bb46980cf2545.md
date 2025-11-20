# Verified Notifications mgt

# Verify Channel in Orion

In order to verify a channel using orion you need to

1. Have an operator (root) session and be logged in with that `sessionId` 
    
    OR alternatively needs to have the permissions for this mutation granted by Orion owners
    
2. call the `verifyChannel` mutation like so:

```graphql
mutation verify {
  verifyChannel(channelIds: ["10","11"]) {
    id                  # channel verification entity id --> not very useful for ops purposes
    channelId           # channel id of the channel just verified
    createdAt           # timestap for the verification
  }
}

```

The return value is an array of the following items:

- `id` of the row in the `Channelverifycation` table
- `channelId` id for the channel verified
- `createdAt` when was the channel verified

In case you are trying to verify an already verified channel, you will get id and creation date of the existing verification in the db and the channel ypp status will remain unchanged

you can check a channel status like so:

```graphql
query checkChannelStatus {
  channels(limit:10) {
    id
    yppStatus {
      __typename
    }
  }
}

```

Examples of responses in Graph QL interface

![Screenshot 2023-11-26 at 12.18.59.png](Verified%20Notifications%20mgt/Screenshot_2023-11-26_at_12.18.59.png)

![Screenshot 2023-11-26 at 12.18.48.png](Verified%20Notifications%20mgt/Screenshot_2023-11-26_at_12.18.48.png)

# Suspend Channel in Orion

Same approach as above but with a different mutation

```graphql
mutation suspendChannelbyId($channelId: String!) {
  suspendChannel(channelId: $channelId) {
    channelId
    createdAt
    id
  }
}

```

As you can see you need as input:

- `channelId` a string in "" containing the channel id to be suspended

And as result you get

- `id` row id of the new `ChannelSuspended` entity created
- `createdAt` timestamp at which suspension has occurred
- `channelId` : id of the channel suspended