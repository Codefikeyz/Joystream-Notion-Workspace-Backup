# Workers & Stake

Created: February 1, 2023 6:06 AM
Tags: Leaderboard, Leads, Stake, Workers, Working Groups (WGs)

```jsx
query MyQuery {
  workers(limit: 1000, where: {}) {
    groupId
    membership {
      handle
    }
    isActive
    isLead
    rewardPerBlock
    stake
  }
}
```

v2 - shows blocks they were hired at, unknown if it shows blocks they were fired at (yet)

```jsx
query MyQuery {
  workers(limit: 1000) {
    groupId
    membership {
      handle
    }
    isActive
    isLead
    rewardPerBlock
    stake
    entry {
      inBlock
    }
    workerexitedeventworker {
      inBlock
    }
  }
}
```