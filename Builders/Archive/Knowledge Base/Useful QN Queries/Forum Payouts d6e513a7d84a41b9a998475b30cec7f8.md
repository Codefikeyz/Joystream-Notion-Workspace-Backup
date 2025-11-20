# Forum Payouts

Created: May 9, 2022 8:33 PM
Description: Get all Forum Worker Payouts
Tags: Forum, Payments, Working Groups (WGs)

```graphql
query ForumWorkersPayouts($councilStartBlock: Int!, $councilEndBlock: Int!) {
  rewardPaidEvents(where: {AND: {group: {name_eq: "forumWorkingGroup"}, inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 100) {
    amount
    worker {
      membership {
        handle
      }
    }
    inBlock
  }
}
```