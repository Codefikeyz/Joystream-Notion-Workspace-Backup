# System

Group: Storage
Attributes: Grade, Group Specific Scores, Subscore
Score: 0.25
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#system_score
Grade Name: SYSTEM_SCORE
Parent Score: Storage Score (Storage%20Score%20cd68026677b9495cb23d38d33a98a0bb.md)
Spot Check Completed: No

```markdown
* The minimum replication rate is 5 (`replication_score`)
* The excess capacity required, for objects and size, must be higher than the "worst" of:

    * 4x last period numbers (not current)
    * 3x the highest period over the last 4 periods (not including current)

    (`excess_capacity_score`)
* Maximum allowed failure probability is 80%, meaning all bags in the top 10% of EITHER:

    * total size stored
    * total objects stored
    * amount of uploads over the last period

    must be able to have at least 80% chance of being able to upload 1 object successfully, despite 2 storage nodes hypotethically being down (`emergency_score)`
* The maximum response time is 2h (`response_score)`

The first three subscores are measured at some point during the last 14400 blocks.

The latter will be measured by creating an opening for `@bwhm` without any rewards, that should be invited to a bucket, but not set to accept new bags, and only (manually) assigned a single existing "testing" bag. If the node goes down, the bag must be removed.

#### Scoring Calculations

Then:

replication_score = 0

// as `Out of 630 bags, 63 are in fewer than 5 buckets`

excess_capacity_score = 1

// looks clearly ok, but stats are missing 

emergency_score = 0

// as `Out of 630 bags, 630 are in fewer than 6 buckets`

response_score = 0

// no opening made/notified

SYSTEM_SCORE = 0.25*(replication_score + excess_capacity_score + emergency_score + response_score)
= 0.25
```

---