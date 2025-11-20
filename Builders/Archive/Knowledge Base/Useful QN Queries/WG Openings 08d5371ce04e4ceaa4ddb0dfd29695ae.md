# WG Openings

Created: February 1, 2023 6:33 AM
Tags: Leaderboard, Openings, Working Groups (WGs)

```jsx
query MyQuery {
  workingGroupOpenings(limit: 1000) {
    id
    groupId
    createdInEvent {
      inBlock
    }
    metadata {
      hiringLimit
    }
    stakeAmount
    unstakingPeriod
    rewardPerBlock
  }
}
```