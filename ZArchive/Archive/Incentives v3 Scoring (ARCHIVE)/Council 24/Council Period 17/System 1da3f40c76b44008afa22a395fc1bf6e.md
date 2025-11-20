# System

Group: Storage
Attributes: Grade, Group Specific Scores, Subscore
JSG Grading Status: Not Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#system_score
Grade Name: SYSTEM_SCORE
Parent Score: Storage Score (Storage%20Score%2015523ef68bc44f70ac3af3c0f60b49c5.md)
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

replication_score = 1

// Note - two bags (2632 and 2635) were under the threshold, but letting it slide.

excess_capacity_score = 0.5

// looks clearly ok, but stats are missing

emergency_score = 0

// See reference below

response_score = 1

// opening was made, so my fault only!

SYSTEM_SCORE = 0.25*(replication_score + excess_capacity_score + emergency_score + response_score)
= 0.25(1+0.5+0+1) = 0.
```

`emergency_score`: The report states:

---

- Filled some information about the `emergency_score`:
    - Users do have at least 80% chance of being able to upload 1 object successfully, despite 2 storage nodes hypotethically being down. See my reasoning:
        - What we have: Currently replication rate is 5, the system has 6 active buckets that accept bags.
        - In our case: 2 storage nodes are down. In worst scenario, there are 3 uploading attempts, 2 of which were dropped by the down storage nodes.
        - Since I test all storage buckets (upload test) on a weekly basis and there is no problems observers, it seems that there is no other obstacles why user can’t upload his object on his 3rd attempt.

---

This seems unrelated to the requested data, and is not correct.