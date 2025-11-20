# Worker Reward updates

Created: February 8, 2023 1:21 AM
Tags: Rewards, Workers, Working Groups (WGs)

```jsx
query MyQuery {
  workerRewardAmountUpdatedEvents {
    id
    groupId
    inBlock
    createdAt
    newRewardPerBlock
    worker {
      membership {
        handle
      }
    }
  }
}
```