# WG Opportunities

Group: HR
JSG Grading Status: Completed
Score: 0.5
Attributes: Grade, Spot Check, Subscore
Grade Name: WORKER_OPPORTUNITIES_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/general-working-group-score#worker-opportunities
Parent Score: General WG Score (General%20WG%20Score%20ffcbe9f8fdbb40a3a552709b92a95b84.md)
Spot Check Completed: No

```markdown
yarn joystream-cli incentives:getOpportunitiesScore -c storageProviders,curators,forum,builders,humanResources,distributors -e 950400 -l 100800 -s 43200 -t 25,25,25,25,25,25

# returns:

This will provide the opportunity scores for round 9,
between blocks 849600 and 950400,
with:
Group: storageProviders, target: 25
Group: curators, target: 25
Group: forum, target: 25
Group: builders, target: 25
Group: humanResources, target: 25
Group: distributors, target: 25
The WORKER_OPPORTUNITIES_SCORE for storageProviders, given a target of 25, is 0.16666666666666666
The WORKER_OPPORTUNITIES_SCORE for curators, given a target of 25, is 1
The WORKER_OPPORTUNITIES_SCORE for forum, given a target of 25, is 0.3333333333333333
The WORKER_OPPORTUNITIES_SCORE for builders, given a target of 25, is 0.3333333333333333
The WORKER_OPPORTUNITIES_SCORE for humanResources, given a target of 25, is 0.5
The WORKER_OPPORTUNITIES_SCORE for distributors, given a target of 25, is 0.125
The LEAD_OPPORTUNITIES_SCORE is 0.14285714285714285, as the lead of the humanResources has had the position for the fewest amount of Council Periods

= 0.5
```