# List all bounties

Created: May 9, 2022 8:27 PM
Description: Show all bounties, status & oracle judgements
Tags: Bounties

```graphql
query {bounties
{id,isTerminated,stage,
workPeriod,judgingPeriod,
judgment{inBlock},
createdInEvent{inBlock},
canceledEvent{inBlock},
createdAt,
createdById,
updatedAt,
updatedById,
}}
```