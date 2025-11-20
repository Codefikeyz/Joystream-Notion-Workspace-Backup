# Storage Report

Group: Storage
JSG Grading Status: Completed
Score: 0.7
Attributes: Document, Forum Post, Grade, Proposal, Report
Forum Link: https://dao.joystream.org/#/forum/thread/164
Forum Report Source: https://dao.joystream.org/#/forum/category/13
Grade Name: REPORT_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#report_score
Notion Link: Storage WG Status Report 8 (https://www.notion.so/Storage-WG-Status-Report-8-bcd6ffb4bb414887b5f7ee8d0752bab2?pvs=21) 
Parent Score: Storage Score (Storage%20Score%20425b22fc33c342e9af5fc54c7e4691f1.md)
Score Type: Subscore
Spot Check Completed: No

In general, requirements for WG Report are going up from the next period. See after the new council parameters are out.

**Questions and comments**

- Report not posted in markdown in the forum, most of it should work fine…
- Some data is outdated, but understandable due to new rules
- Generally ok, but from next period, this report would get a significantly lower score.
- See below for further comments

---

- How many storage buckets were created.
- How many storage buckets were deleted.
- What was the capacity and utilization of each storage bucket at the
beginning and end of the term (number and size of data objects).
    - Not addressed
- How many bags were created.
- How many bags were deleted.
    - Are you sure none was deleted, or assuming all new are new?
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
        - :+1:
- What is the current running costs for the system, and a breakdown of said costs.
- How much bandwidth did the individual nodes consume during the period.
- What, if anything, is the storage group doing the monitor the health of the system.
    - This seems a bit light.
- A list of all `storage` transactions (not `storageProviderWorkingGroup`) made by the lead, and the purpose behind them.
    - None of these are what covering what is requested.