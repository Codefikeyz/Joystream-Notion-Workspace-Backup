# Council Members + Payments

Created: January 16, 2023 12:13 AM
Tags: Council, Leaderboard, Payments

```jsx
query MyQuery {
  councilMembers {
    electedInCouncilId
    accumulatedReward
    id
    member {
      handle
    }
    memberId
    unpaidReward
  }
}
```

v2

```jsx
query MyQuery {
  councilMembers {
    electedInCouncilId
    accumulatedReward
    id
    member {
      handle
    }
    memberId
    unpaidReward
    lastPaymentBlock
    rewardpaymenteventcouncilMember {
      inBlock
      paidBalance
      missingBalance
    }
  }
}
```