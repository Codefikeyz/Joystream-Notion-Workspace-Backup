# Council Budget Refills

Created: May 9, 2022 8:30 PM
Description: Get all Council Budget Refills
Tags: Budgets, Council, Proposals

```graphql
query CouncilMintRefills($councilStartBlock: Int!, $councilEndBlock: Int!) {
  budgetRefillEvents(where: {AND: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 9999) {
    balance
    inBlock
  }
}
```