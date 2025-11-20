# Moderation Score

Group: Content
Attributes: Group Specific Scores, Subscore
Score: 0
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/content-directory-score#moderation_score
Grade Name: MODERATION_SCORE
Parent Score: Content Score (Content%20Score%20ce2d5b2755b340a387e826969753ab5c.md)
Spot Check Completed: No
Subscores: Total Breaches of Policy (Total%20Breaches%20of%20Policy%20d61a5b54dfbb4244a177fe751864c979.md)

**`MODERATION_SCORE`**

Content moderation is applied swiftly and appropriately in accordance with the [Content Policy](https://github.com/Joystream/handbook/blob/master/testnet/content-policy.md).

One spot check performed. The video was not censored within the 24h.

As there is no logging of causes for censoring or uncensoring, this has to stand.

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

= 0
```