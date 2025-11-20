# Council Payment events

Created: January 16, 2023 7:30 AM
Tags: Council, Leaderboard, Payments, Rewards

```jsx
query MyQuery {
  rewardPaymentEvents(limit: 1000) {
    inBlock
    councilMemberId
    id
    paidBalance
    missingBalance
    councilMember {
      electedInCouncilId
      member {
        id
      }
    }
  }
}
```