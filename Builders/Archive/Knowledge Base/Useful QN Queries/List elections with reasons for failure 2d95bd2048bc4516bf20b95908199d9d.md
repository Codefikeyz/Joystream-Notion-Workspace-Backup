# List elections with reasons for failure

Created: July 30, 2022 3:28 PM
Description: List all elections (successful and failed) and give a reason for the failed election if it failed as well as list the blockheight of the election
Tags: Elections, Failures, Voting

```graphql
query {councilStageUpdates(limit: 500)
{id,electedCouncilId,changedAt,
electedCouncil{electedAtBlock,endedAtBlock},
stage {__typename},
electionProblem}

}
```