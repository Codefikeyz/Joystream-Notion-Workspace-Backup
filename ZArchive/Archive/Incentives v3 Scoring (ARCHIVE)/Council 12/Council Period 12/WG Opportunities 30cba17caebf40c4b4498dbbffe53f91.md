# WG Opportunities

Group: Content
Attributes: General WG Score, Grade, Spot Check, Subscore
Score: 1
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/general-working-group-score#worker-opportunities
Grade Name: WORKER_OPPORTUNITIES_SCORE
Parent Score: General WG Score (General%20WG%20Score%20f06980011a00451e994f06bf2b6ad23a.md)
Spot Check Completed: No

Using the [grading tools and resources](../../../Incentives%20Resources%20(ARCHIVE)%20aced0f316e024bb18ac6fac1e8fc80cd.md):

```markdown
yarn joystream-cli incentives:getOpportunitiesScore -c storageProviders,curators,forum,builders,humanResources,distributors,marketing -e 1252800 -l 100800 -s 43200 -t 20,20,20,20,20,20,20
-> 

This will provide the opportunity scores for round 12,
between blocks 1152000 and 1252800,
with:
Group: storageProviders, target: 20
Group: curators, target: 20
Group: forum, target: 20
Group: builders, target: 20
Group: humanResources, target: 20
Group: distributors, target: 20
Group: marketing, target: 20
The WORKER_OPPORTUNITIES_SCORE for storageProviders, given a target of 20, is 0.5
The WORKER_OPPORTUNITIES_SCORE for curators, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for forum, given a target of 20, is 0.16666666666666666
The WORKER_OPPORTUNITIES_SCORE for builders, given a target of 20, is 0.25
The WORKER_OPPORTUNITIES_SCORE for humanResources, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for marketing, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for distributors, given a target of 20, is 0.125
The LEAD_OPPORTUNITIES_SCORE is 1, as the lead of the curators has had the position for the fewest amount of Council Periods
```