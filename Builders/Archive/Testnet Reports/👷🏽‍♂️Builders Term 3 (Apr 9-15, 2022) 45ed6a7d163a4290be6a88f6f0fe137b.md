# 👷🏽‍♂️Builders Term 3 (Apr 9-15, 2022)

### General Status

Figuring out the new processes, ways of working and budgets. 

### Budgeting

Amount of tJOY received in Term: **19M** (via proposals 83, 76, 79)

Salaries spendings: **6,261,991** tJOY

The Squad has a major problem with incorrect budget utilization caused by misunderstanding of how JOY earnings works. As a result, WG has accumulated some debt to its workers. Council did not pass [the bill](https://dao.joystream.org/#/proposals/preview/81) to `sudo` the incorrectly utilized amount back to mint. Lead @isonar is given *carte blanche* to use this amount (~6M tJOY) at his discretion. 

[Payroll](../Time%20Log/Payroll%20d50b756464564d64b335bb7323343a03.md)

*When paying workers, I use the following relation of tJOY to dollar: 1,000 tJOY = 1$ and the basic hourly rate of $30/h. For example, if a worker logged 2h of their working time spent on tasks, it is reasonable to assume that the debt of wages for them is equal to 60,000 tJOY.*

### Hiring

No hiring this term

### Firing

Fired `builders_treasury`

### Development

The issue https://github.com/Joystream/community-repo/issues/744 is under internal review. 

Issue https://github.com/Joystream/pioneer/issues/2793 is in progress. 

Issue https://github.com/Joystream/pioneer/pull/2853 is in external Review. 

### Testing

🥳 Tested - OK https://github.com/Joystream/pioneer/issues/2644 https://github.com/Joystream/pioneer/issues/2353 https://github.com/Joystream/pioneer/issues/2246 https://github.com/Joystream/pioneer/issues/2541 https://github.com/Joystream/pioneer/issues/2651 https://github.com/Joystream/pioneer/issues/2427 https://github.com/Joystream/pioneer/issues/2310 https://github.com/Joystream/pioneer/issues/2544 

Tested- FAIL: https://github.com/Joystream/pioneer/issues/2312 

### Open questions

It seems that [community tooling](../Impact%20of%20Olympia%20on%20Community%20Tools%2092e684153fa0484a84383a38203a2e70.md) developed by the Squad fits the definition of the **public good** quite well. Therefore, the Bounty system can be used to fund them, **in theory**. In practice, however, it is unclear how this works in terms of JOY allocation. @bedeho @Ben Holden-Crowther 

[https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score)

TESTING_SCORE formula is unclear:

`TESTING_SCORE = PIONEER_TEST_SCORE*WORKFLOW_SCORE = [(15 - ISSUES_TESTED_SCORE_i*GRADING_i)/15]*WORKFLOW_SCORE`

DEVELOPMENT_SCORE is unclear: 

`ISSUE_POINTS = Sigma(STORY_POINTS_i)
DEVELOPMENT_SCORE = (10-ISSUE_POINTS)/5`

### Problems

The Squad badly needs QAs. [The opening is there](https://dao.joystream.org/#/working-groups/openings/operationsWorkingGroupAlpha-4).

### Other Feedback

Waiting for feedback on the main [way of working document](../Jsgenesis%20Relations%207a2cbd55bb08430cae90a09faaa810d1.md).

### Queries used to prepare this report

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

```graphql
query WorkersPayouts {
  rewardPaidEvents(where: {AND: {group: {name_eq: "operationsWorkingGroupAlpha"}, inBlock_gte: 244800, inBlock_lt: 345600}}, limit: 100) {
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