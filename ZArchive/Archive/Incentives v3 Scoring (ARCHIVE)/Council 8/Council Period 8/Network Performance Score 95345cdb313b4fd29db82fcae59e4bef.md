# Network Performance Score

Group: Network
Score Status: Completed
Score: 0.623
Attributes: Composite Grade, Overall Grade
Reports Gathered: No
Grade Name: NETWORK_PERFORMANCE_SCORE
Handbook Link: https://github.com/Joystream/handbook/blob/e9747eb6c4501b603f85bd35993faa8a057ac673/testnet/council-period-scoring/README.md#overview
Spot Check Completed: No
Subscores: Builder Score (Builder%20Score%2036d89cfdf7ba4fa8b11bf29a2719c891.md), Content Score (Content%20Score%20fbbf648d080345a5bf8ecfab6eddd357.md), Distributor Score (Distributor%20Score%2060a38ed6753f49ed86214e68c96602e9.md), Storage Score (Storage%20Score%20252ea415198d48d78beeb34b391b9f6f.md), HR Score (HR%20Score%20fbd6395d4fc64558ae4b90f7129c5225.md), Council Period Summary (Council%20Period%20Summary%20651bccc1cfc440f7bb015030f1c24f97.md), Council Period Plan (Council%20Period%20Plan%203f8f1ce826864447a06caa6f92558ae8.md), Lead Opportunities (Lead%20Opportunities%206bf18aa6a58347bcb02b240d6916dc72.md)

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