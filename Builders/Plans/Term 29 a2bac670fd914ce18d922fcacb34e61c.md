# Term 29

## Term 29 plan

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 4 | 306 | `freakstatic` | developer, deputy |
| 11 | 4407 | `TheGrimSavage` | developer |
| 30 | 3089 | `ivant` | QA tester |
| 33 | 37781 | `mkbeefcake` | developer |
| 34 | 2233 | `klaudiusz` | lead |
| 35 | 4404 | `thesan` | developer |
| 36 | 4133 | `mr_bovo` | developer |
| 37 | 4631 | `attemka` | developer |

### 2. **Group budget**

**JOY/USDT EMA30: 0.026** USDT

| **Item** | **USDT** | **JOY** | **Comment** |
| --- | --- | --- | --- |
| Lead salary | $2,134.09 | 82,080.38 JOY | 216,001 blocks * 0.38 JOY = 82,080.38 JOY |
| Dev salaries | $7,425 | 285,576.92 JOY | 1 full-time dev at $3,300/term
1 3/4 time dev at $2,475/term
1 half-time dev at $1,650/term |
| Deputy salary | $700 | 26,923.08 JOY |  |
| QA work | up to $300 | up to 11,538.46 JOY | This will be paid hourly. |
| Bounties | up to $200 | up to 8,333.33 JOY | Up to $200 for Pioneer designs, report will contain a breakdown. |
| Dapplooker | $50 | 1,923.08 JOY |  |
| Total spending | up to $10,166.17 | up to 416,375.25 JOY |  |

### 3. **Group tasks**

1. Continue SWG/DWG support with tooling/infra work as needed. Work with SWG&DWG to deploy at least one squid-based storage and distribution node to production.
2. Continue Nara upgrade operations and ensure smooth upgrade.
3. Deliver WalletConnect support in our apps.
4. Deliver validators dashboard.
5. Continue work on Luxor runtime upgrade.

## Term 29 report

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 4 | 306 | `freakstatic` | developer, deputy |
| 30 | 3089 | `ivant` | QA tester |
| 34 | 2233 | `klaudiusz` | lead |
| 35 | 4404 | `thesan` | developer |
| 36 | 4133 | `mr_bovo` | developer |
| 37 | 4631 | `attemka` | developer |

Following workers were fired because they are no longer regularly working in BWG:

- `TheGrimSavage`
- `ericTron`
- `gyroflaw`
- `mkbeefcake`

### 2. Group budget

**JOY/USDT EMA30: 0.026** USDT

| **Item** | **USDT (planned)** | **USDT (actual)** | **JOY (planned)** | **JOY (actual)** |
| --- | --- | --- | --- | --- |
| Lead salary - 1 | 2,134.09 | 2,285.84 | 82,080.38 | 87,916.80 |
| Dev salaries - 1 | 5,864.33 | 5,385.79 | 225,551.00 | 207,145.85 |
| Deputy salary - 1 | 700.00 | 736.76 | 26,923.08 | 28,336.82 |
| QA work - 2 | 300.00 | 600.00 | 11,538.46 | 23,076.92 |
| Bounties - 3 | 200.00 | 50.00 | 7,692.31 | 1,923.08 |
| Dapplooker - 4 | 50.00 | 50.00 | 1,923.08 | 1,923.08 |
| Past debt - 1 | 260.53 | - | 10,020.20 | - |
| Total spending | 9,508.95 | 9,108.39 | 365,728.61 | 350,322.55 |

Comments:

1. It’s hard to estimate exactly how much was spent covering the past term debt, so I just included past rewards in respective categories totals.
2. $600 was paid to `ivant` for QA work in terms 27-29 - [https://joystream.subscan.io/extrinsic/6390394-1](https://joystream.subscan.io/extrinsic/6390394-1).
3. $50 was paid to `Ayaz05` for Pioneer designs - [https://joystream.subscan.io/extrinsic/6390375-1](https://joystream.subscan.io/extrinsic/6390375-1).
4. [https://joystream.subscan.io/extrinsic/6390352-1](https://joystream.subscan.io/extrinsic/6390352-1).

### 3. Group tasks

> Continue SWG/DWG support with tooling/infra work as needed. Work with SWG&DWG to deploy at least one squid-based storage and distribution node to production.
> 

Done (almost). We have one squid-based distribution node in production, discussing with DWGL to migrate other ones. 2 squid-based storage nodes are currently being set up.

> Continue Nara upgrade operations and ensure smooth upgrade.
> 

Done. Due to continued testing we’ve found a bug in runtime and aborted the upgrade. Then we worked on a fix and more thorough QA on AMM features. At the end of the term we created a new upgrade proposal.

> Deliver WalletConnect support in our apps.
> 

Done partially, we delivered support in Pioneer but Atlas is still being worked on.

> Deliver validators dashboard.
> 

Done.

> Continue work on Luxor runtime upgrade.
> 

Done. Because of Nara abort we’ve had to shift our runtime focus to fixes so we haven’t done that much work on Luxor. Currently we’re scoping out and working on proposal for adjusting validator rewards.

### 4. Other

1. We’ve released a number of minor Pioneer improvements, like ability to create a membership on mobile.
2. We’ve scoped out and started research into community Ethereum bridge:
    1. [https://pioneer.joyutils.org/#/forum/thread/859](https://pioneer.joyutils.org/#/forum/thread/859)
    2. [https://github.com/Joystream/joystream/issues/5084](https://github.com/Joystream/joystream/issues/5084)
3. We’ve investigated upload issues:
    1. Still looking into issues with Colossus nodes
    2. Fixed an issue in Atlas that was causing it to only try to upload to a single operator