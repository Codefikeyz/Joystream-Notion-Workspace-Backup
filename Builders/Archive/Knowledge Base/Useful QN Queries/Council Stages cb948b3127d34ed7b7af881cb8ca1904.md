# Council Stages

Created: May 9, 2022 8:27 PM
Description: List all council stages (idle, announcing, election)
Tags: Council, Elections, Voting

```graphql
query {councilStageUpdates
  {id,createdAt,stage{__typename},changedAt,electedCouncilId,electionProblem}
}
```