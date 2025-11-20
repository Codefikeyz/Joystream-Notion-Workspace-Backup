# Elected Councils

Created: January 31, 2023 12:01 AM
Tags: Council, Elected Councils, Leaderboard

```jsx
query MyQuery {
  electedCouncils {
    id
    electedAtBlock
    endedAtBlock
    isResigned
    councilMembers {
      member {
        handle
      }
    }
  }
}
```