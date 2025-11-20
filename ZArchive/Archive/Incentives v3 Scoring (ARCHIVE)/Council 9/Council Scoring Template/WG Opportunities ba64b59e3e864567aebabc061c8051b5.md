# WG Opportunities

Group: Content
JSG Grading Status: Not Completed
Attributes: Grade, Spot Check, Subscore
Reports Gathered: No
Grade Name: WORKER_OPPORTUNITIES_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/general-working-group-score#worker-opportunities
Parent Score: General WG Score (General%20WG%20Score%206c5cd2a10f36420887b78c57acb64d4a.md)
Spot Check Completed: No

Using the [grading tools](../../../Tools%20and%20Resources%20(ARCHIVE)%208969641b5b284d1c85c658106a79792d.md):

```markdown
yarn joystream-cli incentives:getOpportunitiesScore -c storageProviders,curators,forum,builders,humanResources,distributors -e 849600 -l 100800 -s 43200 -t 20,20,20,20,20,20
# Returns:

This will provide the opportunity scores for round 8,
between blocks 748800 and 849600,
with:
Group: storageProviders, target: 20
Group: curators, target: 20
Group: forum, target: 20
Group: builders, target: 20
Group: humanResources, target: 20
Group: distributors, target: 20
The WORKER_OPPORTUNITIES_SCORE for storageProviders, given a target of 20, is 0.2
The WORKER_OPPORTUNITIES_SCORE for curators, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for forum, given a target of 20, is 0.5
The WORKER_OPPORTUNITIES_SCORE for builders, given a target of 20, is 0.5
The WORKER_OPPORTUNITIES_SCORE for humanResources, given a target of 20, is 1
The WORKER_OPPORTUNITIES_SCORE for distributors, given a target of 20, is 0.2
The LEAD_OPPORTUNITIES_SCORE is 0.16666666666666666, as the lead of the humanResources has had the position for the fewest amount of Council Periods
```