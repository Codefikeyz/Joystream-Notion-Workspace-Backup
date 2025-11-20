# Network Performance Score

Group: Network
Score Status: Calculation
Score: 0.514
Attributes: Composite Grade, Overall Grade
Reports Gathered: No
Grade Name: NETWORK_PERFORMANCE_SCORE
Handbook Link: https://github.com/Joystream/handbook/blob/e9747eb6c4501b603f85bd35993faa8a057ac673/testnet/council-period-scoring/README.md#overview
Handover Weight: 1
Builder Weight: 4
Spot Check Completed: No
Subscores: Builder Score (Builder%20Score%207f23de81598942558b91be6c52c1f4af.md), Content Score (Content%20Score%20509cf368d57b4c37aaad9e7f377ee1c3.md), Distributor Score (Distributor%20Score%2076c92f0fbe3e4590bd3e26d8c30de8bd.md), Storage Score (Storage%20Score%20bdef29f3ae2143378688c425c8a12f94.md), HR Score (HR%20Score%20d203f1ecbf2549489aac1d675ced3ea2.md), Council Period Summary (Council%20Period%20Summary%209cff81e3b5434b0b97ab3307746e23d4.md), Council Period Plan (Council%20Period%20Plan%200eb5242202d04046ac74648aee53c961.md), Lead Opportunities (Lead%20Opportunities%2089f34dced98549cb912eb55b32d1259c.md)
Content Weight: 2
Distributor Weight: 3
Forum Weight: 1
HR Weight: 4
Lead Opportunities Weight: 1
Marketer Weight: 0
Marketing Weight: 0
Plan Weight: 1
Property 1: 2
Property 2: 4
Scoring Weights: Council 7 (../../Council%207%207f116be5a8f54180abd97510bc5cfbc7.md)
Storage Weight: 3
Summary Weight link: 1

```markdown

```

```
NETWORK_PERFORMANCE_SCORE = [
BUILDER_SCORE*B_W +
CONTENT_SCORE*C_W +
DISTRIBUTOR_SCORE*D_W +
FORUM_SCORE*F_W +
HR_SCORE*HR_W +
MARKETER_SCORE*M_W +
STORAGE_SCORE*S_W +
SUMMARY_SCORE*SUM_W +
PLAN_SCORE*P_W +
COUNCIL_MEETING_SCORE*CM_W +
LEAD_OPPORTUNITIES_SCORE*LO_W
]/((B_W + C_W + F_W + D_W + HR_W + M_W + S_W + SUM_W + P_W + CM_W + LO_W)*2^N)

= [
0.533 * 4 +
0.452 * 2 +
0.350 * 3 +
0.633 * 1 +
0.829 * 4 +
(NA * 0)
0.556 * 3 +
0 * 1 +
0 * 1 +
0.900 * 1 +
0.200 * 1
]/((4 + 2 + 3 + 1 + 4 + 0 + 3 + 1 + 1 + 1 + 1)*2^0) = 0.514
```