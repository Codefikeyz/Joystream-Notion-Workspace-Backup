# WG Opportunities

Group: Marketing
Attributes: Document, Forum Post, General WG Score, Grade
Score: 0.25
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/general-working-group-score#worker-opportunities
Grade Name: WORKER_OPPORTUNITIES_SCORE
Parent Score: General WG Score (General%20WG%20Score%20d22743e545a744b89a5d9012f6de9402.md), General WG Score (General%20WG%20Score%20857b3136c02c443d824d6266e657a70b.md)
Spot Check Completed: No

Using the [grading tools and resources](../../../Incentives%20Resources%20(ARCHIVE)%20aced0f316e024bb18ac6fac1e8fc80cd.md):

```markdown
yarn joystream-cli incentives:getOpportunitiesScore -c storageProviders,curators,forum,builders,humanResources,distributors,marketing -e 1051200 -l 100800 -s 43200 -t 25,25,25,25,25,25,25

-> 

This will provide the opportunity scores for round 10,
between blocks 950400 and 1051200,
with:
Group: storageProviders, target: 25
Group: curators, target: 25
Group: forum, target: 25
Group: builders, target: 25
Group: humanResources, target: 25
Group: distributors, target: 25
Group: marketing, target: 25
The WORKER_OPPORTUNITIES_SCORE for storageProviders, given a target of 25, is 0.14285714285714285
The WORKER_OPPORTUNITIES_SCORE for curators, given a target of 25, is 0.5
The WORKER_OPPORTUNITIES_SCORE for forum, given a target of 25, is 0.25
The WORKER_OPPORTUNITIES_SCORE for builders, given a target of 25, is 0.25
The WORKER_OPPORTUNITIES_SCORE for humanResources, given a target of 25, is 0.3333333333333333
The WORKER_OPPORTUNITIES_SCORE for marketing, given a target of 25, is 0.25
The WORKER_OPPORTUNITIES_SCORE for distributors, given a target of 25, is 0.1111111111111111
The LEAD_OPPORTUNITIES_SCORE is 0.2, as the lead of the marketing has had the position for the fewest amount of Council Periods
```