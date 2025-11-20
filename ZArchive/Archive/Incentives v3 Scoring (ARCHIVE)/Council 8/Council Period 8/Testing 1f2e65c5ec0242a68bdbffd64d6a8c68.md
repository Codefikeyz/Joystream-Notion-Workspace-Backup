# Testing

Group: Builders
Score Status: Completed
Score: 0.867
Attributes: Grade, Spot Check, Subscore
Reports Gathered: No
Grade Name: TESTING_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score#testing_score
Parent Score: Builder Score (Builder%20Score%2036d89cfdf7ba4fa8b11bf29a2719c891.md)
Score Type: Subscore
Spot Check Completed: No

From the report: a total of 18 issues tested.

```markdown
TESTING_SCORE:
  If ISSUES_TESTED >= 20:     1
  If 5 < ISSUES_TESTED < 20:  1-((20-ISSUES_TESTED)/15)
  If ISSUES_TESTED =< 5:      0

ISSUES_TESTED=18
1-((20-18)/15)=0.8666666667
```