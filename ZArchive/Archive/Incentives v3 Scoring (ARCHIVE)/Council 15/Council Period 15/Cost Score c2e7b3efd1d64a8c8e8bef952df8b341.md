# Cost Score

Group: Distributors
Attributes: Group Specific Scores, Subscore
Score: 0.4
JSG Grading Status: Completed
Grade Name: COST_SCORE
Spot Check Completed: No

Nothing appears to have been done.

---

```markdown
The cost score will try to measure how the group allocates their resources. Although being cost efficient is not a top priority for a testnet in general, it doesn't make much sense to:

* Employ a lot of operators that are not serving content
* Have operators store significantly less content than their capacity (especially cached capacity)
* Have operators run with costly hardware, and/or in expensive datacenters unless the benefit outweighs the extra costs

The score is the sum of two subscores:

1. A report documenting
   * Current costs
-> 1
   * What can be done to reduce them (without impacting other scores)
-> 0
   * What could be done to reduce them (may impact other scores), and why this may, or may not, be worth it
-> 0
2. A subjective analysis by Jsgenesis, based on the report above and chain data. Any "excessive" costs not covered in the report will reduce the score, whereas costs that are documented will not.  An exeption to this rule is if a "cut" is not enacted in subsequent council periods.&#x20;
-> 0.5
Jsgenesis will assign a score in the range \[0,1] based on this.
```