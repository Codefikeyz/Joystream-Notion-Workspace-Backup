# Election rounds

Created: May 9, 2022 8:27 PM
Description: All election rounds, all cast votes, revealed votes
Tags: Council, Elections, Stake, Voting

```graphql
query {electionRounds
  {id,endedAtBlock,cycleId,castVotes
    {id,castBy,deletedAt,electionRoundId,stake,stakeLocked,voteFor
      {memberId},
      voteForId}
  }
}
```