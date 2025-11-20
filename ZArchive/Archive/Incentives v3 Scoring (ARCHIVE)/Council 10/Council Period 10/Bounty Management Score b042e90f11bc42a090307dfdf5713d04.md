# Bounty Management Score

Group: HR
Attributes: Group Specific Scores, Subscore
Score: 1
JSG Grading Status: Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/human-resources-score#bounty_score
Grade Name: BOUNTY_MANAGEMENT_SCORE
Parent Score: HR Score (HR%20Score%20d320184c34fe4b84aa097a98ee260a87.md)
Spot Check Completed: No

```markdown
yarn joystream-cli incentives:getBountyInfo 950400 1051200
-> 
[
    {
        "inBlock": 1045691,
        "bounty": {
            "id": "64",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 1045609,
        "bounty": {
            "id": "63",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 1045492,
        "bounty": {
            "id": "62",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 1032733,
        "bounty": {
            "id": "61",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 992584,
        "bounty": {
            "id": "56",
            "stage": "Successful",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 992429,
        "bounty": {
            "id": "55",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 988023,
        "bounty": {
            "id": "54",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 962978,
        "bounty": {
            "id": "53",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    },
    {
        "inBlock": 962589,
        "bounty": {
            "id": "52",
            "stage": "Failed",
            "creator": {
                "id": "2502",
                "handle": "adovrn"
            }
        }
    }
]
9 Created.
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
= 9*2 + 0 + 0 = 18 
If    bounty_sum > 10 
BOUNTY_SCORE = 1

If:   bounty_sum <= 10 
BOUNTY_SCORE = bounty_sum/10
```