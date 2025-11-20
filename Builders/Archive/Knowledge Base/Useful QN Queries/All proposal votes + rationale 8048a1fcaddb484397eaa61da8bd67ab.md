# All proposal votes + rationale

Created: February 6, 2023 6:02 AM
Tags: Proposals, Rationale, Votes

```jsx
query MyQuery {
  proposalVotedEvents(limit: 1000) {
    id
    proposalId
    voterId
    voter {
      handle
    }
    rationale
    inBlock
    proposal {
      title
    }
    voteKind
  }
}
```