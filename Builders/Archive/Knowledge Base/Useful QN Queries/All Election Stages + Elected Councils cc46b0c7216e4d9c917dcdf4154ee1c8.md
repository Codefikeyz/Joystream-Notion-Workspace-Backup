# All Election Stages + Elected Councils

Created: February 5, 2023 8:24 PM
Tags: Election Stages, Elections

```jsx
query MyQuery {
  electionRounds {
    id
    isFinished
    referendumStageVoting {
      id
      startedAtBlock
    }
    referendumStageRevealing {
      id
      startedAtBlock
    }
    endedAtBlock
    electedCouncilId
    electedCouncil {
      electedAtBlock
      endedAtBlock
      id
    }
    cycleId
  }
}
```