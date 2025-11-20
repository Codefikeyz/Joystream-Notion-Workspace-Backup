# Network Performance Score

Group: Network
JSG Grading Status: Not Completed
Attributes: Composite Grade, Overall Grade
Reports Gathered: No
Grade Name: NETWORK_PERFORMANCE_SCORE
Handbook Link: https://github.com/Joystream/handbook/blob/e9747eb6c4501b603f85bd35993faa8a057ac673/testnet/council-period-scoring/README.md#overview
Spot Check Completed: No
Subscores: Builder Score (Builder%20Score%20a944639ab3154a6c8820d3a520ac940c.md), Content Score (Content%20Score%2049ef6ba036f84f85a96cc54a97e9fecb.md), Distributor Score (Distributor%20Score%208001afa9bc46453d9d96577079fcff8f.md), Storage Score (Storage%20Score%20dfc2866b23ed424a931819abc445d27c.md), HR Score (HR%20Score%2063185f16d5d74d65a27484bdcf6b6efb.md), Council Period Summary (Council%20Period%20Summary%20020b851ed6cc44a3a3b0e3de52e5ad91.md), Council Period Plan (Council%20Period%20Plan%2077d1ceae0466406aa06b4b9322a6ff50.md), Lead Opportunities (Lead%20Opportunities%206180c751a43948328e6d7045429fd718.md)

```markdown
NETWORK_PERFORMANCE_SCORE = [
BUILDER_SCORE*B_W +
DISTRIBUTOR_SCORE*D_W +
CONTENT_SCORE*C_W +
FORUM_SCORE*F_W +
HR_SCORE*HR_W +
MARKETER_SCORE*M_W +
STORAGE_SCORE*S_W +
SUMMARY_SCORE*SUM_W +
PLAN_SCORE*P_W +
COUNCIL_MEETING_SCORE*CM_W +
LEAD_OPPORTUNITIES_SCORE*LO_W
]/((B_W + C_W + D_W + HR_W + M_W + S_W + SUM_W + P_W + CM_W + LO_W)*2^N)
= [
0.677*8 +
0.639*6 +
0.117*4 +
0.375*1 +
0.805*8 +
0.711*6 +
1*2 +
0.475*2 +
0.706*2 +
0.167*2
]/((8 + 4 + 1 + 6 + 8 + 6 + 2 + 2 + 2 + 2)*2^0) = 0.6225609756
```