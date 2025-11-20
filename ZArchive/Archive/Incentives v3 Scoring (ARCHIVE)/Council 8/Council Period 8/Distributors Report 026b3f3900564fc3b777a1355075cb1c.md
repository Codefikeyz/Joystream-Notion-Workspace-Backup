# Distributors Report

Group: Distributors
Score Status: Completed
Score: 0.9
Score Notes: Basically Perfect
Attributes: Document, Forum Post, Grade, Subscore
Reports Gathered: No
Forum Report Source: https://dao.joystream.org/#/forum/category/15
Grade Name: REPORT_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/distributors-score#report_score
Parent Score: Distributor Score (Distributor%20Score%2060a38ed6753f49ed86214e68c96602e9.md)
Score Type: Subscore
Spot Check Completed: No

Overall, very good and informative.

## Questions and comments

*Per hour perspective*

- This is really useful already as is, but as discussed, would be great to have even more precise data on locations etc.

*Snapshot of current bags per worker nodes:*

- This is not a very useful way of presenting the data.

*A list of all `storage` transactions (not `distributorWorkingGroup`) made by the lead, and the purpose behind them.*

- All of the transactions listed are in fact in the `distributorWorkingGroup` module. Why did no transaction take place?

---

- What was the setup of distribution family buckets, and buckets at the beginning and end of the term.
- What was the dynamic policy at the beginning and end of the term.
- How are bags distributed among the buckets in each bucket family.
- What was the rationale behind the family bucket and bucket configuration, meaning
    - What geographical regions are the families meant to serve
    - Why was the specific dynamic bag policy chosen
    - How do you want to scale the system assuming a growth of 2x, 10x and 100x in terms of data objects and size
- How much bandwidth did the individual nodes consume during the period.
- How is the bandwidth usage distributed, meaning
    - How did bandwidth usage look over a day (peak hours and slow hours)
    - How did bandwidth usage look over a week (peak days and slow days)
    - How did bandwidth usage look across regions (which regions consumes the most, if accessible)
    - How did bandwidth usage look across nodes, operators, buckets and families
- How are distributors supposed to set their `config.yaml` file and why.
- What is the current running costs for the system, and a breakdown of said costs.
- What, if anything, is the group doing the monitor the health of the system.
- A list of all `storage` transactions (not `distributorWorkingGroup`) made by the lead, and the purpose behind them.