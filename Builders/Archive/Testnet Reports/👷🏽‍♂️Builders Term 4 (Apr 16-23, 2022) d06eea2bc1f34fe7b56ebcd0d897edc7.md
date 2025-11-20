# 👷🏽‍♂️Builders Term 4 (Apr 16-23, 2022)

### General Status

Hiring success, new internal incentives system. Meeting with [Dmitry Meltsov](https://www.notion.so/Dmitry-Meltsov-d593051638d64cd0a9009d0dc7f34ee5?pvs=21) on Apr 22nd. 

### Budgeting

WG received no funding this term. 

Salaries spendings: **2,190,145** **tJOY**

Budget remainder at the end of Term: **10,215,284 tJOY**

[Payroll](../Time%20Log/Payroll%20d50b756464564d64b335bb7323343a03.md)

*When paying workers, I use the following relation of tJOY to dollar: 1,000 tJOY = 1$ and the basic hourly rate of $30/h. For example, if a worker logged 2h of their working time spent on tasks, it is reasonable to assume that the debt of wages for them is equal to 60,000 tJOY.*

### Hiring

Hired user **polikosi** as QA. Onboarding in process, slowed down significantly by three-days validators misbehaviour. 

### Firing

no firings this term

### Development

The issue https://github.com/Joystream/community-repo/issues/744 is under internal review. 

Issue https://github.com/Joystream/pioneer/issues/2793 is in progress. 

Issue https://github.com/Joystream/pioneer/pull/2853 is in Merged, task is passed QA. 

Issue https://github.com/Joystream/pioneer/issues/2838 is in Review

### Testing

🥳 Tested - OK https://github.com/Joystream/pioneer/issues/2514

### Open questions

[https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score)

TESTING_SCORE formula is unclear:

`TESTING_SCORE = PIONEER_TEST_SCORE*WORKFLOW_SCORE = [(15 - ISSUES_TESTED_SCORE_i*GRADING_i)/15]*WORKFLOW_SCORE`

DEVELOPMENT_SCORE is unclear: 

`ISSUE_POINTS = Sigma(STORY_POINTS_i)
DEVELOPMENT_SCORE = (10-ISSUE_POINTS)/5`

### Problems

No scoring published! 

No CRM update since April 2

Validators issues caused global disruptions in DAO operations. 

Handover sessions in weekend are inconvenient. 

Low liveness in the WG. 

Slow onboarding by arsi44. 

Issues with l1dev, planned firing, stake slashed at block **399344. Rationale: failure to follow the time logging procedure.** 

### Other Feedback

Unfortunately, according to the **current FM cannot work on Bounties**. So, while Builders still plan to facilitate creation of Bounties related to community tooling (and fund those, if budgets so permit,) the actual progress on them remains a concern due to low developer liveness. 

Planned tripartite session next week to walk through Board 55: @isonar + @Dima + @Martin 

New [internal incentives / bonuses ladder](https://www.notion.so/b22941999af0413e954a5d825885f55d?pvs=21) created (for developers.) 

### Queries used to prepare this report

```graphql
query WorkersPayouts($councilStartBlock: Int!, $councilEndBlock: Int!) {
  rewardPaidEvents(where: {AND: {group: {name_eq: "operationsWorkingGroupAlpha"}, inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 100) {
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

```graphql
query Builders_Budget_Updates($councilStartBlock: Int!, $councilEndBlock: Int!) {
  budgetUpdatedEvents(where: {AND: {
inBlock_gte: $councilStartBlock, 
inBlock_lt: $councilEndBlock, 
group: {name_eq: "operationsWorkingGroupAlpha"}}}, limit: 100) {
    group {
      name
    }
    budgetChangeAmount
    inBlock
  }
}
```