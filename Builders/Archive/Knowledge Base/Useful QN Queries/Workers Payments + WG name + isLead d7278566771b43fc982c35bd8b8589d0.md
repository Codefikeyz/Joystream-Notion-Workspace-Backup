# Workers Payments + WG name + isLead

Created: January 11, 2023 4:59 AM
Tags: Leaderboard, Leads, Payments, Workers, Working Groups (WGs)

```jsx
query MyQuery {
  rewardPaidEvents(limit: 1000) {
    inBlock
    id
    amount
    paymentType
    worker {
      membership {
        handle
      }
      missingRewardAmount
      isLead
      groupId
    }
  }
}
```