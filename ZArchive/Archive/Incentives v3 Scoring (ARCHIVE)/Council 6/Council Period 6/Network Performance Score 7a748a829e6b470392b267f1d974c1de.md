# Network Performance Score

Group: Network
Score Status: Ready for review
Score: 0.612
Attributes: Composite Grade, Overall Grade
Reports Gathered: No
Grade Name: NETWORK_PERFORMANCE_SCORE
Handbook Link: https://github.com/Joystream/handbook/blob/e9747eb6c4501b603f85bd35993faa8a057ac673/testnet/council-period-scoring/README.md#overview
Spot Check Completed: No
Subscores: Builder Score (Builder%20Score%20b1cb26ff0c95494298f594c5c9f29bbe.md), Content Score (Content%20Score%20c634a6221d584e519cb09f82dfd95a0a.md), Distributor Score (Distributor%20Score%20998f4998e98247aab958933b3ca7bd9e.md), Storage Score (Storage%20Score%2081b017cd1afa4f8b9ceebde3f66d7d6a.md), HR Score (HR%20Score%209fd43cc681f94368a75567de8fb0b903.md), Council Period Summary (Council%20Period%20Summary%20980e48608d964850b36fd4f7569726f0.md), Council Period Plan (Council%20Period%20Plan%20152c64cd4ae44ff4875b56d2b6e57e89.md), Lead Opportunities (Lead%20Opportunities%20435db2cc7aca4111bddfc088e3b70ffa.md)

```markdown
NETWORK_PERFORMANCE_SCORE = [
BUILDER_SCORE*B_W +
DISTRIBUTOR_SCORE*D_W +
CONTENT_SCORE*C_W +
HR_SCORE*HR_W +
MARKETER_SCORE*M_W +
STORAGE_SCORE*S_W +
SUMMARY_SCORE*SUM_W +
PLAN_SCORE*P_W +
COUNCIL_MEETING_SCORE*CM_W +
LEAD_OPPORTUNITIES_SCORE*LO_W
]/((B_W + C_W + D_W + HR_W + M_W + S_W + SUM_W + P_W + CM_W + LO_W)*2^N)

= [
0.613 * 4 +
0.609 * 3 +
0.188 * 2 +
0.830 * 4 +
0.502 * 3 +
1.000 * 1 +
1.000 * 1 +
0.500 * 1 +
0.250 * 1]/((4+3+2+4+3+1+1+1+1)*2^0) = 0.612

```