# Bounty Management Score

Group: HR
Attributes: Group Specific Scores, Subscore
Score: 1
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/human-resources-score#bounty_score
Grade Name: BOUNTY_MANAGEMENT_SCORE
Parent Score: HR Score (HR%20Score%20f282b71f1e514de5be6809072e19e6c1.md)
Spot Check Completed: No

7 made, but only 5 in the report

```markdown
yarn joystream-cli incentives:getBountyInfo 
```

- `initial_newcomer_bounties` be the amount of bounties
created on chain for someone that joined the discord within the last 4
weeks, and has never had a role or been assigned a bounty
- `returning_member_bounties` be the amount bounties
created on chain, and assigned to a member that has never had any role
or been assigned a bounty on the current chain
- `wg_role_bounties` be the amount of bounties created on
chain, and assigned to a member that wants to join a specific working
group, and needs the pass the WG screening bounty. More info in the
general working group [#bounty-score](https://github.com/Joystream/handbook/blob/master/testnet/council-period-scoring/general-working-group-score.md#bounty-score) and [#opening-score](https://github.com/Joystream/handbook/blob/master/testnet/council-period-scoring/general-working-group-score.md#opening-score).
- `bounty_sum` be the weighted sum of each
- `bounty_target` be the target of bounties created

```markdown
bounty_sum = initial_newcomer_bounties*2 + returning_member_bounties + wg_role_bounties
= 
If    bounty_sum > 10 
BOUNTY_SCORE = 1

If:   bounty_sum <= 10 
BOUNTY_SCORE = bounty_sum/10

All five for newcomers -> 1
```