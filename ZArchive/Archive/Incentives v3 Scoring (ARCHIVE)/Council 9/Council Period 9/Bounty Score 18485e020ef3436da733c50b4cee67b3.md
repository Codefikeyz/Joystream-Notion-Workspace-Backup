# Bounty Score

Group: HR
JSG Grading Status: Completed
Score: 1
Grade Name: BOUNTY_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/human-resources-score#bounty_score
Parent Score: HR Score (HR%20Score%200d725a2e93344db29ba568de6312d77a.md)
Score Type: Subscore
Spot Check Completed: Yes

From what I can see:

`initial_newcomer_bounties` = 9

`returning_member_bounties` = 1

`wg_role_bounties` = 0

```markdown
Is a function of bounties created by the HR group, that gets assigned to someone with in the CRM. Although the primary focus is on newcomers joining the #start-here channel, two other "groups" of users also count.
Scoring Calculations

Let:

    initial_newcomer_bounties be the amount of bounties created on chain for someone that joined the discord within the last 4 weeks, and has never had a role or been assigned a bounty
    returning_member_bounties be the amount bounties created on chain, and assigned to a member that has never had any role or been assigned a bounty on the current chain
    wg_role_bounties be the amount of bounties created on chain, and assigned to a member that wants to join a specific working group, and needs the pass the WG screening bounty. More info in the general working group #bounty-score and #opening-score.
    bounty_sum be the weighted sum of each
    bounty_target be the target of bounties created

bounty_sum = initial_newcomer_bounties*2 + returning_member_bounties + wg_role_bounties
= 9*2+1+0 = 19
-> 1

If    bounty_sum > 10 
BOUNTY_SCORE = 1

If:   bounty_sum <= 10 
BOUNTY_SCORE = bounty_sum/10
```

`