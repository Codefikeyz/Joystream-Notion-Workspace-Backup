# Testing

Group: Builders
Attributes: Grade, Group Specific Scores, Spot Check, Subscore
JSG Grading Status: Not Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/builders-score#testing_score
Grade Name: TESTING_SCORE
Parent Score: Builder Score (Builder%20Score%20c35bc64d5f6c49849749c4c1f8de3eef.md)
Spot Check Completed: No

```markdown
TESTING_SCORE:
  If ISSUES_TESTED >= 15:     1
  If 5 < ISSUES_TESTED < 15:  ISSUES_TESTED/15
  If ISSUES_TESTED =< 5:      0

ISSUES_TESTED = 11
-> 0.7333333333
```