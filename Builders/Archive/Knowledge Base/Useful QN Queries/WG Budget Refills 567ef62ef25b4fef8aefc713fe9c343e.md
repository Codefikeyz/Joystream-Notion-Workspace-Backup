# WG Budget Refills

Created: May 9, 2022 8:31 PM
Description: Get all WGs Budget Refills
Tags: Budgets, Proposals, Working Groups (WGs)

```graphql
query WG_BudgetUpdated($councilStartBlock: Int!, $councilEndBlock: Int!){
  budgetUpdatedEvents(where: {AND: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 9999) {
    group {
      name
    }
    budgetChangeAmount
    inBlock
  }
}
```