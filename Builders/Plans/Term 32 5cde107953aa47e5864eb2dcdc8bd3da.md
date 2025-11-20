# Term 32

## Term 32 plan

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 4 | 306 | `freakstatic` | developer, deputy |
| 30 | 3089 | `ivant` | QA tester |
| 34 | 2233 | `klaudiusz` | lead |
| 35 | 4404 | `thesan` | developer |
| 36 | 4133 | `mr_bovo` | developer |
| 37 | 4631 | `attemka` | developer |

### 2. **Group budget**

**JOY/USDT EMA30: 0.021** USDT

*Note: new term length is 28 days. 28/30 = 0.933. This multiplier will be used for monthly salaries.*

| **Item** | **USDT** | **JOY** | **Comment** |
| --- | --- | --- | --- |
| Lead salary | 9,330.00 | 444,285.71 | $10,000/mo * 0.933 = $9,330/term. With 1yr vesting applied. |
| Dev salaries | 7,212.19 | 343,437.61 | `thesan` dev at 1/2 time = $3,300/mo = $3,079/term `mr_bovo` dev ($6,600-$2,170)/mo=$4,430/mo = $4,133.19/term `attemka` at $0/term |
| Deputy salary | 1,119.60 | 53,314.29 |  |
| Total spending | 17,661.79 | 841,037.61 |  |

### 3. **Group tasks**

1. Continue work on S3 storage for Colossus.
2. Ship maintenance mode for Argus and Colossus nodes.
3. Continue work on the bridge. If possible, develop the runtime pallet and propose a runtime upgrade before term end.

## Term 32 report

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 4 | 306 | `freakstatic` | developer, deputy |
| 30 | 3089 | `ivant` | QA tester |
| 34 | 2233 | `klaudiusz` | lead |
| 35 | 4404 | `thesan` | developer |
| 36 | 4133 | `mr_bovo` | developer |
| 37 | 4631 | `attemka` | developer |

### 2. Group budget

**JOY/USDT EMA30: 0.021** USDT

| **Item** | **USDT (planned)** | **USDT (actual)** | **JOY (planned)** | **JOY (actual)** |
| --- | --- | --- | --- | --- |
| Lead salary - 1 | 9,330.00 | 9,330.00 | 444,285.71 | 444,285.71 |
| Dev salaries - 2, 3 | 6,288.42 | 6,157.63 | 299,448.57 | 293,220.34 |
| Deputy salary - 2 | 1,119.60 | 1,084.11 | 53,314.29 | 51,624.41 |
| Total spending - 3 | 16,738.02 | 16,571.74 | 797,048.57 | 789,130.46 |

Comments:

1. 1yr vesting was applied.
Vested budget spending: [https://joystream.subscan.io/extrinsic/7300979-1](https://joystream.subscan.io/extrinsic/7300979-1)
During the term I have also discovered that my lead salary for previous term was for incorrect amount. I have returned the difference to the budget: [https://joystream.subscan.io/extrinsic/7301095-1](https://joystream.subscan.io/extrinsic/7301095-1)
2. At the end of the term the group has ran out of funds and accrued a bit of debt. That’s because of the council plan for term 32 specifying slightly lower budget than planned spending.
3. 69,014.26 JOY was returned to BWG budget by `mr_bovo` for the days he was not working during terms 31 and 31: [https://joystream.subscan.io/extrinsic/7415160-1](https://joystream.subscan.io/extrinsic/7415160-1). This amount was not subtracted from the spending breakdown above.

### 3. Group tasks

> Continue work on S3 storage for Colossus.
> 

Work is progressing nicely, main development is almost done. We will start testing early next term.

> Ship maintenance mode for Argus and Colossus nodes.
> 

Not shipped. We have tested the functionality and found some issues and reported those to JSG as they were doing the development. Unfortunately after reporting the issues, no fixes were made, as JSG is probably focused on other things. We will try to take over the development of this feature and prepare the fixes within the BWG next term.

> Continue work on the bridge. If possible, develop the runtime pallet and propose a runtime upgrade before term end.
> 

Work is progressing without any major issues. The runtime pallet development is mostly finished, but we’re still testing it so it wasn’t possible to submit the runtime upgrade. We have finished development and tests for Ethereum smart contracts and they were deployed to Sepolia testnet. We have also started work on indexer that will track status of transfers across Joystream and Ethereum chains.

### 4. Other

1. We’ve successfully finished Luxor runtime upgrade including infra upgrades and minor fixes for Pioneer.
2. WalletConnect support for Gleev was shipped.
3. We’ve investigated some Gleev-related SEO issues and prepared a fix for videos being marked by Google as explicit: [https://discord.com/channels/811216481340751934/1035131444080680971/1237116143664365680](https://discord.com/channels/811216481340751934/1035131444080680971/1237116143664365680)
4. We’ve done improvements to council report tool (not yet deployed, in review):
    1. Improving reliability and report generation time: [https://github.com/Joystream/council-report-tool/pull/4](https://github.com/Joystream/council-report-tool/pull/4)
    2. Adding CRT stats to the reports: [https://github.com/Joystream/council-report-tool/pull/5](https://github.com/Joystream/council-report-tool/pull/5)
5. We’ve provided support to Content WG for CRT analytics.