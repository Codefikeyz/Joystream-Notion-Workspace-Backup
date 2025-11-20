# Moderation Score

Group: Content
JSG Grading Status: Completed
Score: 0.182
Grade Name: MODERATION_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/content-directory-score#moderation_score
Parent Score: Content Score (Content%20Score%20a3aabbae48374ae9b6f6933504efed94.md)
Spot Check Completed: No
Subscores: Response Score (Response%20Score%2017aa349466b649ae81600aee4664bfd2.md), Total Breaches of Policy (Total%20Breaches%20of%20Policy%20708defc211554e779ec574ee5b55a938.md)

The videos marked “to be censored” from the last report:

[https://play.joystream.org/video/26742](https://play.joystream.org/video/26742)

[https://play.joystream.org/video/26743](https://play.joystream.org/video/26743)

[https://play.joystream.org/video/26741](https://play.joystream.org/video/26741)

[https://play.joystream.org/video/26745](https://play.joystream.org/video/26745)

[https://play.joystream.org/video/26748](https://play.joystream.org/video/26748)

[https://play.joystream.org/video/26754](https://play.joystream.org/video/26754)

were all censored - :+1:

Although not clear whether any or all videos censored were actually in violation of the policies, the censored videos with seconds from creation to censorship then id:

```markdown
good censor 35232000 26795
good censor 35412001 26794
good censor 35838000 26793
bad censor 91908000 26785
bad censor 92016000 26784
bad censor 92130000 26783
bad censor 92256000 26782
bad censor 92430000 26781
bad censor 92525998 26780
good censor 49458000 26779
bad censor 95250000 26778
bad censor 181379997 26776
bad censor 200856000 26775
bad censor 213522000 26774
bad censor 226752000 26773
bad censor 302508000 26771
bad censor 326502000 26754
bad censor 506586000 26748
bad censor 603840000 26745
bad censor 613458000 26743
bad censor 613416000 26742
bad censor 613824000 26741
```

---

Spotchecks: 

- [https://play.joystream.org/video/26776](https://play.joystream.org/video/26776)
    - Video was censored, but appears ok → [https://www.youtube.com/watch?v=X5Syf3GaE6A](https://www.youtube.com/watch?v=X5Syf3GaE6A) (reuse allowed)
- [https://play.joystream.org/video/26784](https://play.joystream.org/video/26784)
    - Don’t see why this was censored? All “Joystream Official” videos are CC0

### Scoring Calculations

Let:

- `RESPONSE SCORE` be equal to:
- `1` when a sanction is applied within 24 hours of a policy breaching item* being uploaded
- `0` when no action is taken within 24 hours of a policy breaching item* being uploaded
*identified by Jsgenesis during the period
- `TOTAL_BREACHES_OF_POLICY` be the total number of instances of policy breaching items seen uploaded by Jsgenesis.

Then:

```markdown
MODERATION_SCORE = (SUM(RESPONSE_SCORES)/TOTAL_BREACHES_OF_POLICY)
= 4/22 = 0.1818181818
```