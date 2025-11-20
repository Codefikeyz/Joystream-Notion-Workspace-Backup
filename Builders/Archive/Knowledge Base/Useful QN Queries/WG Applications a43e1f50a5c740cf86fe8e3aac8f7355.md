# WG Applications

Created: February 1, 2023 6:29 AM
Tags: Applications, Leaderboard, Working Groups (WGs)

```jsx
query MyQuery {
  workingGroupApplications(limit: 1000) {
    id
    stake
    applicantId
    openingId
    createdInEvent {
      inBlock}
    workerapplication {
      isActive
      membership {
        handle
      }
      application {
        workerapplication {
          id
        }
      }
    }
  }
}
```