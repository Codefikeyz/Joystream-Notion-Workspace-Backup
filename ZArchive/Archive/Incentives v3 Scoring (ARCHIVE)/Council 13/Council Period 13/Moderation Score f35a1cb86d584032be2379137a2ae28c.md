# Moderation Score

Group: Content
Attributes: Group Specific Scores, Subscore
Score: 0.5
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/content-directory-score#moderation_score
Grade Name: MODERATION_SCORE
Parent Score: Content Score (Content%20Score%20c264de5c24ac4e1eb1499e23ba0af73d.md)
Spot Check Completed: No
Subscores: Total Breaches of Policy (Total%20Breaches%20of%20Policy%20ebe75b2c9a5a4e5cb1346e3b321b5a2a.md)

**`MODERATION_SCORE`**

**From before**

*Content moderation is applied swiftly and appropriately in accordance with the [Content Policy](https://github.com/Joystream/handbook/blob/master/testnet/content-policy.md).*

*Not clear what to do here, as I don’t want to keep on punishing for one old video, with no new spot checks performed.*

Going forward, the following will be done:

- For each censor:
    - If ok (justification on notion) + 0.5
    - If NOT ok (justification on notion) → 0 anyway
    - If in within 24h + 0.5
    - If no links to when or where - 0.5

### Scoring Calculations

Let:

- `response_time_i` be the time (in hours) from a video `i` is published until an action has been taken.
- `justification_j` be a score in the range [0,1], set by Jsgenesis staff for a few selected actions, based on:
    - the justification provided for the action, such as pointing to the
    rule or guideline that is violated, proof related to license, etc.
    - the `rationale` included in the `content.updateVideoCensorshipStatus` extrinsic
    - further logging, such as the blockheight/event/[link to explorer](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/explorer) and who made the decision
    - whether or not the justification/`rationale` is true

```markdown
response_time_score_i:
  response_time_i >= 4:          1
  response_time_i < 24:          0
  4 < response_time_i < 24:      -0.05*response_time_i + 1.2
  
MODERATION_SCORE = [ sum(response_time_score_i) / i + sum(justification_j) / j] / 2

---
From comments:
= 0.5

No spotcheck
```