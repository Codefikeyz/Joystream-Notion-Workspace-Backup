# Budget funded by member events

Created: February 27, 2023 11:34 AM
Tags: Budgets, Working Groups (WGs)

```jsx
query MyQuery {
  budgetFundedEvents(limit: 1000) {
    id
    amount
    groupId
    inBlock
    member {
      handle
    }
    rationale
    createdAt
  }
}
```