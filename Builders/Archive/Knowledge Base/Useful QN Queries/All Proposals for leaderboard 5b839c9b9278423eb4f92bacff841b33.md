# All Proposals for leaderboard

Created: January 15, 2023 4:32 AM
Tags: Council, Funding, Leaderboard, Proposals

```jsx
query MyQuery {
  proposals(limit: 1000, orderBy: createdAt_ASC) {
    id
    councilApprovals
    statusSetAtBlock
    isFinalized
    createdInEvent {
      inBlock
    }
    status {
      __typename
    }
    title
    details {
      __typename
      ... on FundingRequestProposalDetails {
        __typename
        destinationsList {
          destinations {
            amount
          }
        }
      }
    }
  }
}
```