# HR Score

Group: HR
Attributes: Composite Grade, Master Score
JSG Grading Status: Not Completed
Handbook Link: https://github.com/Joystream/handbook/blob/master/testnet/council-period-scoring/human-resources-score.md#score
Grade Name: HR_SCORE
Parent Score: Network Performance Score (Network%20Performance%20Score%202dcdb268a15b464cbbf7d75f1c9654e2.md)
Spot Check Completed: No
Subscores: General WG Score (General%20WG%20Score%20013008c6907b4c58b3b9535d85c996e2.md), HR Report (HR%20Report%209d74b0c423cb4be0b2b5958b0535d1bf.md), Response Time (Response%20Time%20bf2fa933a25747b39f76a6a88acf4cee.md), Person Logging Score (Person%20Logging%20Score%205ac1627869f045909f5304862123a3ab.md), Interaction Logging Score (Interaction%20Logging%20Score%201c6ac0fb4fc54c048e0c9a45517dab4f.md), Bounty Management Score (Bounty%20Management%20Score%20248c3a5403f04c1b99f2c3fb34bb06f3.md)

```markdown
HR_SCORE = [2*GENERAL_WG_SCORE + REPORT_SCORE + 2(RESPONSE_TIME_SCORE) + PERSON_LOGGING_SCORE + INTERACTION_LOGGING_SCORE + BOUNTY_MANAGEMENT_SCORE]/(8*2^{N})
= [2*0.667 + 0.95 + 2*(1) + 0.667 + 1 + 1]/(8*2^{0}) = 0.868875
```