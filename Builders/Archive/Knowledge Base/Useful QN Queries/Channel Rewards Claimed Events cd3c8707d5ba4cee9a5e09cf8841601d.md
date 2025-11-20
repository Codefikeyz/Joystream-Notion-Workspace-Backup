# Channel Rewards Claimed Events

Created: July 10, 2023 1:54 PM
Description: Claimed rewards by channel
Tags: Channels, Payments, Rewards

```jsx
query MyQuery {
  channelRewardClaimedEvents(limit: 5000) {
    amount
    channel {
      title
      cumulativeRewardClaimed
    }
    channelId
    inBlock
  }
}
```