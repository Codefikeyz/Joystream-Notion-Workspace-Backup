# Lead Opportunities

Group: Council
JSG Grading Status: Completed
Score: 0.143
Attributes: Grade
Grade Name: LEAD_OPPORTUNITIES_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring#lead-opportunities
Parent Score: Network Performance Score (Network%20Performance%20Score%20b5d67b08236940ae8249140591d8fe47.md)
Score Type: Main Score
Spot Check Completed: No

Using the [grading tools](../../../Tools%20and%20Resources%20(ARCHIVE)%208969641b5b284d1c85c658106a79792d.md):

```markdown
arn joystream-cli incentives:getOpportunitiesScore -c storageProviders,curators,forum,builders,humanResources,distributors -e 950400 -l 100800 -s 43200 -t 25,25,25,25,25,25
# Returns:

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
```