# Council Member payouts

Created: May 9, 2022 8:29 PM
Description: Get all payouts for Council Members
Tags: Council, Payments

```graphql
query CouncilSalaryPayouts($councilStartBlock: Int!, $councilEndBlock: Int!)  {
  rewardPaymentEvents(where: {AND: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 9999) {
    inBlock
    paidBalance
    rewardAccount
    missingBalance
  }
}
```