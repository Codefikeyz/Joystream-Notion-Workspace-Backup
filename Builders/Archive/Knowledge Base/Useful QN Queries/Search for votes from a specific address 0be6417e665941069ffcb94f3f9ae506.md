# Search for votes from a specific address

Created: June 2, 2022 1:36 PM
Tags: Elections, Voting

```graphql
query {
  voteCastEvents(where: {castVote: {castBy_eq: "5CDCqEbzTiyxpaNGEK7M7wzEvwrjY6rQpM2Np5zm2nFPEVfj"}}) {
    castVote {
      stake
      voteFor {
        memberId
        stake
        status
      }
      castBy
      electionRoundId
    }
    inBlock
  }
}
```