# Storage Report

Group: Storage
JSG Grading Status: Not Completed
Attributes: Document, Forum Post, Grade
Reports Gathered: No
Forum Report Source: https://dao.joystream.org/#/forum/category/13
Grade Name: REPORT_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#report_score
Parent Score: Storage Score (Storage%20Score%20dfc2866b23ed424a931819abc445d27c.md)
Score Type: Subscore
Spot Check Completed: No

As before, overall really elaborate and informative. The few spotchecks came out clean :) 

## Notes and Comments

*A list of all storage transactions (not storageProviderWorkingGroup) made by the lead, and the purpose behind them.*

- Why are no `storage` transactions taking place?
- Although `ifconfig` is a decent short term solution, and a good indication of relative use (between terms) it needs to be improved.

---

- How many storage buckets were created.
- How many storage buckets were deleted.
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).
- How many bags were created.
- How many bags were deleted.
- What data objects were permanently lost, and if any, why.
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