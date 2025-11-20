# WG Spending

Created: June 17, 2022 10:50 PM
Description: payout from budget (non JOY-able)
Tags: Working Groups (WGs)

During a period with known start and end

```jsx
query { budgetSpendingEvents (where: {inBlock_gt: 1051200, inBlock_lt: 1152000 }, limit: 10000) { inBlock amount groupId }}
```

All with rationale

```jsx
query { budgetSpendingEvents (limit: 10000) { inBlock amount groupId rationale reciever }}
```