# Term 33

## Term 33 plan

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

**JOY/USDT EMA30: 0.015** USDT

*Note: new term length is 28 days. 28/30 = 0.933. This multiplier will be used for monthly salaries.*

| **Item** | **USDT** | **JOY** | **Comment** |
| --- | --- | --- | --- |
| Lead salary | 9,330.00 | 622,000 | $10,000/mo * 0.933 = $9,330/term. With 1yr vesting applied. |
| Dev salaries | 5,672.64 | 378,176 | `thesan` dev at 1/4 time = $1,650/mo = $1,539.45/term `mr_bovo` dev ($6,600-$2,170)/mo=$4,430/mo = $4,133.19/term |
| Deputy salary | 1,119.60 | 74,640 |  |
| Total spending | 16,122.24 | 1,074,816 |  |

### 3. **Group tasks**

1. Ship S3 storage support for Colossus.
2. Ship maintenance mode for Argus and Colossus nodes.
3. Continue work on the Argo bridge. Propose Petra runtime upgrade including:
    1. Argo runtime pallet
    2. Adjustments for funding proposal: [https://pioneer.joyutils.org/#/proposals/preview/554](https://pioneer.joyutils.org/#/proposals/preview/554)

## Term 33 report

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

**JOY/USDT EMA30: 0.015** USDT

| **Item** | **USDT (planned)** | **USDT (actual)** | **JOY (planned)** | **JOY (actual)** |
| --- | --- | --- | --- | --- |
| Lead salary - 1 | 9,330.00 | 9,330.00 | 622,000 | 622,000 |
| Dev salaries | 5,672.64 | 5,456.96 | 378,176 | 363,797.64 |
| Deputy salary | 1,119.60 | 1,077.65 | 74,640 | 71,843.6 |
| Total spending | 16,122.24 | 15,864.62 | 1,074,816 | 1,057,641.25 |

Comments:

1. 1yr vesting was applied.
Vested budget spending: [https://joystream.subscan.io/extrinsic/7817484-1](https://joystream.subscan.io/extrinsic/7817484-1)

### 3. Group tasks

> Ship S3 storage support for Colossus.
> 

🟡 The main development was done and the PR was opened: [https://github.com/Joystream/joystream/pull/5150](https://github.com/Joystream/joystream/pull/5150). We didn’t get around to reviewing it yet because of the focus on Petra upgrade. We’ve requested help from JSG to review this but no response so far.

> Ship maintenance mode for Argus and Colossus nodes.
> 

🔴 No progress this term, we’ve focused on bigger priorities.

> Continue work on the Argo bridge. Propose Petra runtime upgrade.
> 

🟢 Petra upgrade has been finished and proposed: [https://pioneerapp.xyz/#/proposals/preview/905](https://pioneerapp.xyz/#/proposals/preview/905). Work on the bridge is also progressing very nicely, we have an MVP ready including Joystream, Ethereum, indexer and app components, which allows to transfer tokens. We still need to integrate Joystream and Ethereum multisigs into the app and polish it up.

### 4. Other

1. We’ve finalized Metamask implementation for Pioneer and created a PR for Atlas integration.
2. We’ve added email notifications for proposal discussions in Pioneer.