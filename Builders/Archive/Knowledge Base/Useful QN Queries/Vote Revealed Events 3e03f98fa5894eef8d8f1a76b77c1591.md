# Vote Revealed Events

Created: May 9, 2022 8:27 PM
Description: Lists all revealed votes, address of those who voted, current status of stake (locked or not) and election round
Tags: Elections, Voting

```graphql
query {voteRevealedEvents
  {inBlock,id,castVoteId,castVote{electionRoundId,stake,votePower,stakeLocked,commitment,voteForId,
    voteFor{id,memberId,votePower}
  }}
}
```