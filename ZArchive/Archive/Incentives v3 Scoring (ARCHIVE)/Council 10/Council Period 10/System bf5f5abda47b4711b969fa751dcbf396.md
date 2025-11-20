# System

Group: Distributors
Attributes: Grade, Group Specific Scores, Spot Check, Subscore
Score: 0
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/distributors-score#system_score
Grade Name: SYSTEM_SCORE
Parent Score: Distributor Score (Distributor%20Score%20501417c8484f41d48b43e07d82170356.md)
Spot Check Completed: No

```markdown
All subscores are graded binary

coverage_score = 0
redundancy_score = 0
version_score = 0
// only 2/14 running latest (0.1.2)
transparancy_score = 0
excess_capacity_score = 0
excess_capacity_score = 0
response_score = 0
// No opening

  SYSTEM_SCORE = (1/6)*(coverage_score + redundancy_score + version_score + transparancy_score + excess_capacity_score + response_score)
	= 0
```

Although well intended and partially correct given the purpose of `bucket_families` , the current system causes issues for many reasons, two of which are easy to fix:

- Buckets are assigned more bags than they should, and needs to fetch
objects from a storage provider themselves, before they can serve them
- High latency between user, the player/orion and the distributor nodes, given most users residing in eurasia

Redesign the distributor system, to reduce these errors.

### Parameters

- All families/buckets well distributed across Europe and the CIS (`coverage_score`)
- All objects must be available from at least 2 buckets in each family
    - The top 10 most videos must be available from at least 3 buckets in each family (`redundancy_score`)
- All distributor nodes are on the latest version of `argus` (`version_score`)
- All distributor nodes displays their location coordinates and node capacity in the metadata, (`transparancy_score`)
- No distributor node stores more than 60% of their capacity (`excess_capacity_score`)
- The maximum response time is 2h (`response_score)`

The first five subscores are measured at some point during the last 14400 blocks.

The latter will be measured by creating an opening for `@bwhm`
 without any rewards, that should be invited to a bucket and set as 
serving, but not accept any bags. If the node goes down, it must be set 
to not serving.