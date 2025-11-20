# Storage Report

Group: Storage
Attributes: Document, Forum Post, Grade, Group Specific Scores, Proposal, Report
Score Notes: On time
Score: 0.947
Submitted [Block]: 1263914
JSG Grading Status: Data input - grading req
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#report_score
Forum Link: https://dao.joystream.org/#/forum/thread/303
Forum Report Source: https://dao.joystream.org/#/forum/category/13
Grade Name: REPORT_SCORE
Parent Score: Storage Score (Storage%20Score%203968f349f7b845b9820cbd3eac936a96.md)
Spot Check Completed: No

**Questions and comments**

- As always, the “old” stats are correct and well presented
- Missing information about `elasticSearch`! Good to see the guide (for deployment), but stats are missing.
- Simple count: 18/19 points.
    - Only big issue the lack of system score info.
    

General question: Why are so many storage nodes not accepting new data? This seems like a giant waste of money for the council?

---

- How many storage buckets were created.
- How many storage buckets were deleted.
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).
    - Nice to see this addressed!
- How many bags were created.
- How many bags were deleted.
- What data objects were permanently lost, and if any, why.
    - Nice to also see an attempt to explain this!
- How many data objects were (attempted) uploaded, and
    - what was their total size,
    - what was the size distribution.
- List of failed data upload upload attempts on chain, and if possible to find out - why.
    - If this is not done, the `UPLOAD_SCORE` will assume all uploads failed independently, and that the group is at fault.
- A chart (with raw data available for future use) that plots the
changes in the values below over the council period, through snapshots
at every 600 block:
    - data objects, number and size;
    - amount of bags;
    - (average) number and size of data objects in a bag
- What is the current running costs for the system, and a breakdown of said costs.
- How much bandwidth did the individual nodes consume during the period.
- What, if anything, is the storage group doing the monitor the health of the system.
- A list of all `storage` transactions (not `storageProviderWorkingGroup`) made by the lead, and the purpose behind them.
- The values used as inputs for the subscores `excess_capacity_score` and `emergency_score` under the `SYSTEM_SCORE`.
    - Not addressed: `excess_capacity_score`
        - This is a rather large task.
    - Partially addressed: `emergency_score`, but this doesn’t really make sense.