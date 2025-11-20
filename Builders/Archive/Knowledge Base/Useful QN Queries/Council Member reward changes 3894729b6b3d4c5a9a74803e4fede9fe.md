# Council Member reward changes

Created: June 2, 2022 1:54 PM
Tags: Council, Payments

```graphql
query {councilorRewardUpdatedEvents(where: {AND: {inBlock_gte: 900000, inBlock_lt: 1100000}}, limit: 9999) {
    
    inBlock
  }
}
```