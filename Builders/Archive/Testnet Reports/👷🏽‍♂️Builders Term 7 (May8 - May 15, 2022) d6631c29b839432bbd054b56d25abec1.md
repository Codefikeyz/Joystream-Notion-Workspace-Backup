# 👷🏽‍♂️Builders Term 7 (May8 - May 15, 2022)

### Testing Score Formula [no change]

`TESTING_SCORE:
If ISSUES_TESTED >= 20:     1
If 5 < ISSUES_TESTED < 20:  1-((20-ISSUES_TESTED)/15)
If ISSUES_TESTED =< 5:      0`

### General Development Score Formula [no change]

`DEVELOPMENT_SCORE:
If STORY_POINTS >= 15:      1
If STORY_POINTS < 15:  1-((15-STORY_POINTS)/15)`

### Pioneer Development Score Formula [no change]

`DEVELOPMENT_SCORE:
If STORY_POINTS >= 12:      1
If STORY_POINTS < 12:  1-((10-STORY_POINTS)/12)`

# **Working Group Score key points**

## 💵 Accounting of how much was spent on what.

Budget at Term start: **22M** tJOY

Budget received: **20M** tJOY - Proposal `#164`

Wages paid: **7,215,540** tJOY

Unpaid: **8M** tJOY ⛔️ Council hesitated to compensate Lead @isonar for this work. Proposal `#162` 

Discretionary spendings: none

Budget at Term end: **35M** tJOY

Debt at Term end: **1,322,091** tJOY - I believe this is incorrect as the number stays the same for the last couple of terms. 

Additional info - see [Payouts](https://docs.google.com/spreadsheets/d/10t76A69v6LBEwxb8WP82Z5MhTRUm7l0aDvsbDsXMw1w/edit?usp=sharing) document.

## Actual hires made (if any)

no hirings made this week. 

## Actual slashes imposed (if any)

None

## Actual firings were done (if any)

fired 1 worker (plutoniumApples)

## Propose a set of bounties that newcomers can tackle.

Newcomers are directed at `Bounty Dev Backlog` column in the Project 55. No need to create new ones.

## Changes made to the Builders notion board

Updated the JSG relations protocol: [https://joystream.notion.site/Jsgenesis-Relations-7a2cbd55bb08430cae90a09faaa810d1](../Jsgenesis%20Relations%207a2cbd55bb08430cae90a09faaa810d1.md)

Created [Proxy PO](../Proxy%20Product%20Owner%20Responsibilities%2023e563c16cfc41f39f960b2d63e875c7.md) responsibilities document.

## Summary of how well the working group served its intended purpose

1. 👍🏿 Good traction in Project 55. 
2. 👍🏿 Working Group Bot released.
3. 👎 No sync with Martin this week

## Recommendations for what should be focused on in the next council period in order to make the group more effective

1. ***Councils l1dev and maxlevush should be issued a warning for sabotaging Builders budgeting proposals.*** 

## Suggested changes

Suggested changes to the purpose or practices built into this working group, other working groups, the council, or JSGenesis' role, in order to increase the overall effectiveness of the group or the project: 

- Staging environment has 24h long election periods, takes too much time to set things up. Suggesting to `sudo` the shorter cycles.
- Suggesting to remove [Markdown support issue](https://github.com/Joystream/pioneer/issues/2712) from Community backlog and move it to core JSG backlog.
- Given the low current developers activity it is highly unlikely that the Squad will deliver on both Pioneer and Community backlogs every Term. Suggesting the following process: if there is no planned activity for Project 56, Lead to give Martin an advance heads up, Martin  to remove General Development from the scoring formula for the next term.

# All information your **WG Scores** ask for

### 🔧 Pioneer Development

Was in progress, but returned to To Do due to assignee unresponsive

1. [https://github.com/Joystream/pioneer/issues/2303](https://github.com/Joystream/pioneer/issues/2303) test bounty assigned to Github user eikebartels (1 SP)

Work postponed:

1. [https://github.com/Joystream/pioneer/issues/2712](https://github.com/Joystream/pioneer/issues/2712) assignee jameswee (5 SP)

In progress:

1. [https://github.com/Joystream/pioneer/issues/2362](https://github.com/Joystream/pioneer/issues/2362) assignee freakstatic (3 SP)
2. https://github.com/Joystream/pioneer/issues/2735 2SP, jameswee
3. #2509, 1SP, jameswee [https://github.com/Joystream/pioneer/issues/2509](https://github.com/Joystream/pioneer/issues/2509)

**Completed in Term 6, but PR merged in Term 7:** 

1. #2864, 2 SP, jameswee, 4h: [https://github.com/Joystream/pioneer/issues/2864](https://github.com/Joystream/pioneer/issues/2864)
2. #2689, 2 SP, jameswee, 3h: ([https://github.com/Joystream/pioneer/issues/2689](https://github.com/Joystream/pioneer/issues/2689))
3. #2884, 2 SP, lkskrn, 3h: ([https://github.com/Joystream/pioneer/issues/2884](https://github.com/Joystream/pioneer/issues/2884))
4. #2821, 2 SP, lkskrn, 3h: ([https://github.com/Joystream/pioneer/issues/2821](https://github.com/Joystream/pioneer/issues/2821))

✅  Total: 8 SP

**In Review by JSG**

1. #2349, 2SP, jameswee [https://github.com/Joystream/pioneer/issues/2349](https://github.com/Joystream/pioneer/issues/2349)

### 🔧 General Development

✅  [1 task, 8 SP, by isonar (20h spent in Term 6)](https://github.com/Joystream/community-repo/issues/754) Complete. Deployed to production (Heroku)

⛔️ Council hesitated to compensate Lead @isonar for this work. Proposal `#162` 

### 🤖 Testing

Tested - OK: **`13 tickets`**

polikosi (5.5h) - 2672, 2639, 2203, 2825, 2655, 2487, 2737, 2410
ivant (2.5h) - 2919, 2983, 2278, 2561, 2701

Failed QA: 2413 (**`1 Ticket`**)

Total tickets: **`14`**

QA hours in total: `8`

### 🦾 Team Performance

# All actions you took and results to solve the group tasks the Council gave you in Term Goals & Group Priorities

- Action 1
- Action 2