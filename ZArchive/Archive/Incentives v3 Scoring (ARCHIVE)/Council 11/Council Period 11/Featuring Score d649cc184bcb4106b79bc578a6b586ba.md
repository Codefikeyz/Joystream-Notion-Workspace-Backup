# Featuring Score

Group: Content
Attributes: Group Specific Scores, Subscore
Score: 0.444
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/content-directory-score#featuring_score
Grade Name: FEATURING_SCORE
Parent Score: Content Score (Content%20Score%20004119f9e07b44c9a77b2e142972c598.md)
Spot Check Completed: No

```markdown
CATEGORIES_SCORE = max[(HERO_CATEGORIES_CHANGE + VIDEO_CATEGORIES_CHANGE)/4 , 1]
= 0

HERO_SCORE = max[(HERO_CHANGE + HERO_CHANGE_QUALITY)/4 , 1]
= max[(4 + 1)/4 , 1] = 1
//Missing from which (here) video to which, and more granular "when"

LOGGING_SCORE = 0.333
//Missing from which (here) video to which, and more granular "when"

  # finally
  FEATURING_SCORE = (CATEGORIES_SCORE + HERO_SCORE + LOGGING_SCORE)/3
= 1.333/3 = 0.444
```

- `CATEGORIES_SCORE` be the score for updating the main featured categories on the platform, as a function of:
    - `HERO_CATEGORIES_CHANGE` be the amount of times all heros were changed during the council period
    - `VIDEO_CATEGORIES_CHANGE` be the amount of times the top video(s) in each categories were changed during the council period
- `HERO_SCORE` be the score for updating the main featured video on the platform, as a function of:
    - `HERO_CHANGE` be the amount of times the hero was changed during the council period
    - `HERO_CHANGE_QUALITY` be the subjective score of how well this is done, based on how frequently the same video is rotated back to the top, whether the "teaser" and metadata is correct, and whether the
    video is appropriate to feature (eg. good/bad video, not NSFW, etc.)
        - Note that Jsgenesis reserves the right to veto videos suggested for
        this position, as it's the first thing a new user sees, and should thus
        be of really high quality
- `LOGGING_SCORE` be the quality of the change logs in the
notion board, so that grading can be done without having to check
manually every day. This means creating a spreadsheet/table/db/json that every time a change is made