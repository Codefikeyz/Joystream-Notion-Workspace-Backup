# WG Budget Refill Events

Created: January 29, 2023 7:09 AM
Tags: Budgets, Leaderboard

```jsx
query MyQuery {
  budgetUpdatedEvents(limit: 1000) {
    groupId
    budgetChangeAmount
    inBlock
    id
  }
}
```