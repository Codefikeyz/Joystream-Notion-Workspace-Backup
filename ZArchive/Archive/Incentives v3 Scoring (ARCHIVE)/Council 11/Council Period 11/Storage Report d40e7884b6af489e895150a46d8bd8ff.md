# Storage Report

Group: Storage
Attributes: Document, Forum Post, Grade, Group Specific Scores, Proposal, Report
Score Notes: On time
Score: 0.868
Submitted [Block]: 1146810
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#report_score
Forum Link: https://dao.joystream.org/#/forum/thread/247
Forum Report Source: https://dao.joystream.org/#/forum/category/13
Grade Name: REPORT_SCORE
Parent Score: Storage Score (Storage%20Score%20afb78d52beb24d74965d2df84f748f5c.md)
Spot Check Completed: No

**Questions and comments**

- As always, the “old” stats are correct and well presented
- Some later points are ignored, but nice to see it’s read :D
- Great to see `elasticSearch`!
- Simple count: 16.5/19 points.
    - I want to emphasize the importance of the newer stuff, but still good!

---

- How many storage buckets were created.
- How many storage buckets were deleted.
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).
    - Not addressed
- How many bags were created.
- How many bags were deleted.
- What data objects were permanently lost, and if any, why.
    - Not addressed (why)
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
    - Not addressed