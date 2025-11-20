# WG Discretionary Spending

Created: January 30, 2023 6:34 AM
Tags: Leaderboard, Spending, Working Groups (WGs)

```jsx
query MyQuery {
  budgetSpendingEvents(limit: 1000) {
    id
    groupId
    inBlock
    rationale
    amount
  }
}
```