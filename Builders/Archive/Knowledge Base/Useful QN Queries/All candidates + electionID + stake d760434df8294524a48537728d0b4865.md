# All candidates + electionID + stake

Created: January 15, 2023 3:46 AM
Tags: Council, Elections, Leaderboard

```jsx
query MyQuery {
  candidates(limit: 500) {
    id
    electionRoundId
    memberId
    member {
      handle
    }
    stake
    stakeLocked
    status
    electionRound {
      electedCouncilId
    }
    candidacynoteseteventcandidate {
      inBlock
    }
  }
}
```