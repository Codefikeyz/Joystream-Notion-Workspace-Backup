# WG Opportunities

Group: Distributors
Attributes: General WG Score, Grade, Spot Check, Subscore
Score: 0.333
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/general-working-group-score#worker-opportunities
Grade Name: WORKER_OPPORTUNITIES_SCORE
Parent Score: General WG Score (General%20WG%20Score%20b50cc6380c984136b3e49b7188bace41.md)
Spot Check Completed: No

```markdown
joystream-cli incentives:getOpportunitiesScoreFixed -c storageProviders,curators,forum,builders,humanResources,distributors,marketing -e 1483200 -s 43200 -l 144000,244800,345600,446400,547200,648000,748800,849600,950400,1051200,1152000,1252800,1382400,1483200 -t 20,20,20,20,20,20,20
-> 

This will provide the opportunity scores for round 14,
between blocks 1382400 and 1483200,
with:
Group: storageProviders, target: 20
Group: curators, target: 20
Group: forum, target: 20
Group: builders, target: 20
Group: humanResources, target: 20
Group: distributors, target: 20
Group: marketing, target: 20
The WORKER_OPPORTUNITIES_SCORE for storageProviders, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for curators, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for forum, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for builders, given a target of 20, is 0.3333333333333333
The WORKER_OPPORTUNITIES_SCORE for humanResources, given a target of 20, is 0.5
The WORKER_OPPORTUNITIES_SCORE for marketing, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for distributors, given a target of 20, is 0.3333333333333333
The LEAD_OPPORTUNITIES_SCORE is 0.5, as the lead of the curators has had the position for the fewest amount of Council Periods
```