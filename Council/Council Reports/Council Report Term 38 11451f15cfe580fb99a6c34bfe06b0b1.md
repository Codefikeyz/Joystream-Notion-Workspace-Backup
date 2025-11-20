# Council Report Term 38

Date: August 29, 2024 → September 27, 2024
Council Term: 37
Testnet / Mainnet: Mainnet

## Council Report

- Dates: 27 September 2024 → 25 October 2024
- Council Term: 00000012
- Start block: 9,432,030 0x395c0de3d0c10d03986b0d9eb3e1ae02424b504a30a2d65c4fce4449747da474
- End block: 9,835,230 0x9807d08b7abc82241435effdad39ec87004ec442b21f683d54d4664bfb28662e

## 1. Composition

- **leet_joy**, 49%
- **klaudiusz**, 17%
- **0x2bc**, 2%

Election results: [https://pioneerapp.xyz/#/election/past-elections/00000012](https://pioneerapp.xyz/#/election/past-elections/00000012)

## 2. General stats

- Channels: **67** (total **29,888**)
- Videos: **5,589** (total **1,423,778**)
- Forum threads: **10** (total **997**)
- Forum posts: **40** (total **7,083**)
- Proposals: **17** (total **1,031**)
- Memberships: **338** (total **65,604**)

## 3**. Term Highlights**

- This term [chief council experiment](https://pioneerapp.xyz/#/forum/thread/972) continues, where all three winning candidates in the election adhered to the agreed-upon structure.
- 10,000 channels were opted our from YPP due to [yt-sync issue](https://github.com/Joystream/youtube-synch/issues/337)
- Lezek was hired as DAO [CTO](https://pioneerapp.xyz/#/working-groups/openings/operationsWorkingGroupAlpha-38) at October 8. [Summary on technical isssues/tasks](https://docs.google.com/spreadsheets/d/1OGxo8ranpirLSjWFbLh-rmqgaU0Q9wGGN8oox4D5q1c/edit?gid=0#gid=0) done by Lezek.
- JoystreamERC20 was listed officially on [CoinMarketCap](https://www.coingecko.com/en/coins/joystream), [CoinGecko](https://www.coingecko.com/en/coins/joystream), [BaseScan](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c), etc
- JOY was listed on new Indonesian exchange [Triv](https://triv.co.id/id/markets/JOY_IDR)
- DAO [added more funds](https://app.safe.global/transactions/tx?safe=base:0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747&id=multisig_0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747_0x3ab0c13b4e36e686f72c0641e0daba236ed24d796afd76042d84f07c0b0d1e11) to LP on Uniswap v3
- [Argo bridge parameters](https://pioneerapp.xyz/#/proposals/preview/926) updated: minting limits of BASE [increased to 3M JOY](https://pioneerapp.xyz/#/proposals/preview/1022) per day and the delay for timelock governance [increased to 5 days](https://app.safe.global/transactions/tx?safe=base:0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747&id=multisig_0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747_0x4d6d546734305f7e08aee805713d56818123d5e67b64021eccbedaf11f23eef8).
- The Council decided to drop OKRs, replacing process-heavy meetings and evaluations with direct daily communication and core metrics tracking, as daily standups already do a great job aligning our small team with less overhead
- An interesting fact: this was the first term in mainnet with negative inflation, due to JOY tokens being burned and bridged to BASE by users
- A proposal to reduce council members rewards were [expired](https://pioneerapp.xyz/#/proposals/preview/1006) (one of cm forgot to cast their votes)
- MWG reached out to [Aerodrome finance](https://aerodrome.finance/) team and submitted a WL (October 11) [application](https://discord.com/channels/1139239009772642416/1293972642717630620) for listing
- Kdembler presented a transcoding Proof of Concept (POC) at [https://transcoder-app.vercel.app/](https://transcoder-app.vercel.app/), which allows users to upload videos that are transcoded to H264 1080p and stored, though advanced features like multiple resolutions and adaptive streaming are not yet implemented. https://github.com/joyutils/transcoder

**Challenges**

- **10,000 channels were opted our from YPP:** A recent switch from YouTube's video downloading tool (yt-dlp) to their official API resulted in over 10,000 channels being inadvertently opted out of the system due to expired authentication tokens, causing widespread confusion among content creators about their program participation status. https://github.com/Joystream/youtube-synch/issues/337
- While the team is evaluating two potential solutions - either reverting affected channels' status using HubSpot data or returning to yt-dlp with improved IP management - the CTO advises that both options present significant challenges: the unofficial yt-dlp approach risks legal issues and constant IP blocking from YouTube, while the official API route would require user reauthorization and may face strict usage limits, suggesting that either solution will require dedicated development resources for long-term maintenance.
- Jsgenesis [emphasizes](https://discord.com/channels/811216481340751934/1035125759687266364/1296412656353284127) that this issue requires dedicated development resources beyond the current capacity and suggests that fixing this syncing problem should be prioritized by the DAO over new feature development to ensure the YPP program's continued functionality. It was decided that the builders will investigate this issue after developing the archive node script.

## 4**. Tasks Status**

**CDN Optimization**: Work with the infrastructure lead on scaling down the content delivery costs; facilitate USDT server compensation for workers.

*Note: At the beginning of the term, the council initiated discussions with the infrastructure lead on cost reduction. It was agreed to add this as a working group task, as we examined nodes that potentially brought no value to CDN but had high costs. The council also investigated the possibility and complications of deleting certain video files from the Joystream library through CWG. It was decided to remove certain servers, and workers were informed in advance. The newly hired builders' lead started work on SWG support  ([Colossus cleanup issue](https://github.com/Joystream/joystream/pull/5191) and [Archive Script](https://discord.com/channels/811216481340751934/812344874099277824/1295332375257157662)). A solution for archiving the library is expected to be reviewed and implemented in the first week of Term 39, which will allow SWG to reduce replication rates with minimal risks.*

**Hiring**: Assess the need for hiring new working group leads (AWG, CWG, and BWG), considering the current low liquidity market and its impact on the DAO's finances, and facilitate the hiring process.

*Note: Due to the resignation of the previous BWGL, it was decided to create an opening for the CTO role on October 3. Lezek was hired for the role and started work.*

**OKRs**: Conduct Q3 review, finalize and pass the proposal for Q4.

*Note: The Council decided to drop OKRs, replacing process-heavy meetings and evaluations with direct daily communication and core metrics tracking, as daily standups already do a great job aligning our small team with less overhead*

**Roadmap Update**: Reassess prioritization of future developments based on current DAO resources; evaluate potential impact of these developments on MCAP and PMF; update and push new .json to joystream.org.

*Note: V5 was merged to website.*

**YPP Operations**: Facilitate creator payouts; ensure creator support via Discord, email, and GitHub tickets; work on resolving current issues such as pending channel status.

*Note: Jenny was assigned to handle creator payouts this term and requested Hubspot API access for better visibility, while HRWG requested email access from the previous CWG team for support purposes. Due to yt-sync issues the number of channels to receive payments were nearly 0.*

**YPP Costs**: Assess program spending; adjust payout amounts if needed.

*Note: In progress, it was impossible to properly evaluate program spending due to temporary [yt-sync issues](https://github.com/Joystream/youtube-synch/issues/337).*

***Marketing**: Scale up the Joystream ambassador program; ann*ounce Phase 3; increase program budgets.

*Note: In progress.*

**Apps**: Support initiatives improving Atlas documentation and tutorials on launching an app; continue with marketing research and develop strategies to attract potential builders to create applications on top of the protocol.

## 5**. WGs’ Status**

**Legends**:
*🟢 Completed*

*🟡 Started but not completed / WIP*

*🔴 No work was done or not achieved*

### **Builders WG**

Lead: Lezek

[Plan](https://pioneerapp.xyz/#/forum/thread/62?post=7057) - Report (WIP)

*Note: This was Lezek's first term as BWGL. Their first action items as the new lead included an operational handover with the previous BWGL, Council, Infrastructure Lead, and other parties. Then, Lezek prepared a breakdown of technical issues and estimated delivery times. The Council decided to prioritize supporting Infrastructure Working Groups as the initial development tasks ([Colossus cleanup issue](https://github.com/Joystream/joystream/pull/5191) and [Archive Script](https://discord.com/channels/811216481340751934/812344874099277824/1295332375257157662)).*

### **Storage WG**

Lead: Freakstatic

[Plan](https://pioneerapp.xyz/#/forum/thread/879?post=7061) - Report (WIP)

- Maintain a replication rate of not lower 2 for all objects.
- Maintain percentage of unaccepted objects < 2%.
- Maintain percentage of lost objects 0%.
- Maintain a storage system availability of 100%

*Note: Smooth operations, some workers are in the process of migrating to a cheaper server. Workers were paid with USDT on Ethereum for their servers.*

### **Distribution WG**

Lead: Freakstatic

[Plan](https://pioneerapp.xyz/#/forum/thread/85?post=7055) - Report (WIP)

- Pay pending payments of the previous term
- Onboard the new lead
- Investigate about cost for each macro region, @mrbovo (previous lead) left some recommendations here [https://github.com/Joystream/joystream/issues/5186#issue-2498720521](https://github.com/Joystream/joystream/issues/5186#issue-2498720521) and propose new salary ad hoc for each region (see issue)

*Note: Smooth operations, some workers are in the process of migrating to a cheaper server.*

### **HR WG**

Lead: **Codefikeyz**

[Plan](https://pioneerapp.xyz/#/forum/thread/119?post=7043) - [Report](https://pioneerapp.xyz/#/forum/thread/108?post=7082) 

*🟢* Information Dissemination including council election facilitation, daily updates postings and EMA30 value announcement

*🟢* Publication of Weekly Summary

*🟢* Meetings and engagement coordination and moderation

*🟢* Review Salaries following the passed proposals related(for example: DAO Leave Policy and EMA30 Cap)

*🟢* Discord and Faucet Management

Additional:

*🟢* Take full responsibility for supporting YPP Creators, including handling email and GitHub tickets. Seek council help when needed.

### **Content WG**

Lead: NA

*🟢* Content Moderation across all homepage feed categories and marketplaces

*🟢* YPP program support for verification

### **Marketing WG**

Lead: **leet_joy**

[Plan](https://pioneerapp.xyz/#/forum/thread/68?post=7045) - [Report](https://pioneerapp.xyz/#/forum/thread/46?post=7083)

*🟡* Ambassador program promotion and management

5 ambassadors were excluded from the program; 

Phase 3 is in development, and the Marketing Working Group has worked on assets, structure, and a content calendar along with a marketing plan for launch.

*🟡* Social media content management

*🟢* CMC communities campaign

Due to some YouTube sync issues, the Marketing Working Group was not able to get the best content for posting on CMC communities. However, we are still using some good quality older videos for posting. The MWG is also promoting Joystream-related posts (eg. [~100K impressions](https://coinmarketcap.com/community/post/342479640/)) on CMC using own affiliate accounts.

*🟢* Region-based campaigns R&D

Following [CIS video platforms research](https://pioneerapp.xyz/#/forum/thread/976), Marikjudo worked on a market strategy for the region. While it was not finished and properly translated, the draft can be [viewed here](https://docs.google.com/document/d/14njmA02sWpfCgq7K-S5VU_4xMi6j5kXmNFT55x0Bl8Y/edit?tab=t.0).

*🟢* Listings of wrapped JOY

A significant amount of work was put into listing our BASE asset on various platforms. JoystreamERC20 was listed officially on [CoinMarketCap](https://www.coingecko.com/en/coins/joystream), [CoinGecko](https://www.coingecko.com/en/coins/joystream), [BaseScan](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c), Coinbase wallet, etc

*🟢* Listing of wrapped JOY on Aerodrome DEX

MWG reached out to Aerodrome team and submitted a WL (October 11) [application](https://discord.com/channels/1139239009772642416/1293972642717630620) for listing.

## 6**. Budget**

### **Overview**

- Starting Council budget: **14,579,873.537 JOY**
- Spending from Council budget: **2,603,153.333 JOY**
- Refill of Council budget: **4,667,600 JOY**
- Ending Council budget: **16,644,320.203 JOY**

**Other Assets**

- [SAFE](https://pioneerapp.xyz/#/proposals/preview/497) (Ethereum mainnet):  **8,977 USDT**
- [ETHAdmin](https://pioneerapp.xyz/#/proposals/preview/961) (BASE): Uniswap Liquidity NFTs **~$18.12K value**
- DAO VCC: **1,660.46 USDT**

**Inflation**

- Start issuance: **1,088,997,867.998 JOY + 2,025,630 JOY** ([base network](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c))
- End issuance: **1,087,137,898.65 JOY + 7,072,559 JOY** ([base network](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c))
- Term issuance: **3,272,971 JOY**
- Term issuance: **0.367%**
- JOY burned (bridged to other chains): **5,046,929 JOY**
- JOY burned (fees and commissions): **86,012.084 JOY**

**Table 6.1. Inflation**

| Term | Minted, MJOY | Inflation |
| --- | --- | --- |
| 1 | 0.453 | 0.045 % |
| 2 | 0.909 | 0.091 % |
| 3 | 3.056 | 0.306 % |
| 4 | 1.274 | 0.127 % |
| 5 | 1.414 | 0.141 % |
| 6 | 1.822 | 0.182 % |
| 7 | 1.491 | 0.149 % |
| 8 | 1.451 | 0.145 % |
| 9 | 1.666 | 0.167 % |
| 10 | 1.329 | 0.133 % |
| 11 | 1.313 | 0.131 % |
| 12 | 2.087 | 0.209 % |
| 13 | 2.013 | 0.201 % |
| 14 | 1.575 | 0.158 % |
| 15 | 1.834 | 0.183 % |
| 16 | 2.157 | 0.216 % |
| 17 | 1.677 | 0.168 % |
| 18 | 1.761 | 0.176 % |
| 19 | 1.642 | 0.164 % |
| 20 | 1.648 | 0.165 % |
| 21 | 1.744 | 0.174 % |
| 22 | 2.477 | 0.248 % |
| 23 | 2.517 | 0.252 % |
| 24 | 1.666 | 0.167 % |
| 25 | 1.776 | 0.178 % |
| 26 | 1.476 | 0.148 % |
| 27 | 1.46 | 0.146 % |
| 28 | 1.576 | 0.158 % |
| 29 | 1.811 | 0.181 % |
| 30 | 1.63 | 0.163 % |
| 31 | 4.118 | 0.412 % |
| 32 | 4.671 | 0.467 % |
| 33 | 6.259 | 0.626 % |
| 34 | 6.812 | 0.681% |
| 35 | 7.281 | 0.0728% |
| 36 (both Joy L1 and Base) | 6.480 | 0.604% |
| 37 | 3.683 | 0.368 % |
| 38 | 3.272 | 0.367% |
| **Total**  | 94.21 | 9.421% |

**Table 6.2. Overall Budget**

| **Item** | **Total spending (planned), JOY** | **Total spending (actual), JOY** |
| --- | --- | --- |
| Council rewards | 933,333.00 | 933,333.333 |
| WG spending, incl: | 1,513,073.61 | 1,086,936.403 |
| Funding proposals | 600,000.00 | 61,820 |
| Validator rewards | 1,200,000.00 | 1,190,882 |
| Term issuance, Gross | 4,246,406.61 | 3,272,971.736 |
| Tokens bured | 150,000.00 | (5,132,941.084) |
| Term issuance, Net | 4,096,406.61 | -1,859,969.348 |

*Note: Token burns showed a large amount due to the usage of the Argo bridge app, as some users sent/burned **5,046,929 JOY** on the Joystream Network and moved them to BASE. JOY burned by fees and commissions was **86,012.084 JOY**.*

**Table 6.3. WGs’ Workers**

| Working group | Workers number (incl Lead) | Workers hired | Workers fired | Workers left |
| --- | --- | --- | --- | --- |
| Builders | 2 | 1 | 1 | 0 |
| Storage | 6 | 0 | 0 | 0 |
| Distribution | 7 | 0 | 0 | 0 |
| Forum | 1 | 0 | 0 | 0 |
| Apps | 0 | 0 | 0 | 0 |
| Content | 3 | 0 | 0 | 1 |
| HR | 5 | 0 | 0 | 0 |
| Membership | 0 | 0 | 0 | 0 |
| Marketing | 6 | 0 | 1 | 0 |
| Total | 30 | 1 | 2 | 1 |

### **Table 6.4. WGs’ Budgets, JOY**

| **Working group** | **Start budget, JOY** | **Refilled, JOY** | **Spending (planned), JOY** | **Spending (actual), JOY** | **Workers rewards, JOY** |
| --- | --- | --- | --- | --- | --- |
| Builders | 354,887.095 | 200,000 | 0 | 0.002 | 0 |
| Storage | 37,033.267 | 200,000 | 165,286.97 | 165,286.97 | 165,286.97 |
| Distribution | 219,016.659 | 200,000 | 270,000.00 | 137,293.041 | 0 |
| Forum | 1,015.952 | 0 | 0 | 0 | 0 |
| Apps | 0 | 0 | 0 | 0 | 0 |
| Content | 6,433.419 | 0 | 0 | 0 | 0 |
| HR | 432.593 | 208,000 | 203,866.64 | 203,866.64 | 0 |
| Membership | 0 | 0 | 0 | 0 | 0 |
| Marketing | 288,836.541 | 800,000 | 873,920.00 | 580,489.749 | 36,329.749 |
| Total | 907,655.528 | 1,608,000 | 1,513,073.61 | 1,086,936.403 | 201,616.719 |

Notes:

- For a full breakdown of each working group's expenses, refer to Section 5. Each working group's status includes a link to the lead's report.
- The column titled `Spending (actual), JOY` represents the actual amounts spent by each working group, primarily on salaries. For the Marketing WG, this also covers various initiatives. The `Workers rewards, JOY` column shows the amount of JOY paid to workers per block. Currently, most DAO workers are paid through discretionary spending, which is not reflected in the table.
- This term, the BWG has not executed salary payments. This is because the lead is new and occupied with other responsibilities.
- *YPP payouts were near 0 due to issue with YouTube syncing.*
- Token burns showed a large amount due to usage of the Argo bridge app, as some users sent/burned **5,046,929 JOY** on the Joystream Network and moved them to BASE.
- The Content WG appears to have no spending because the working group lacks a lead, who is the only one capable of paying workers from the WG budget. As a workaround, workers were paid through a series of funding proposals.
- Most salaries in the working groups are USD-denominated and subject to vesting schedules (determined at the beginning of each term) and an EMA30 limit, which was implemented this term. Consequently, the salaries do not reflect the current token price as they are affected by the EMA30 cap and vesting.
- The Council [used 500K JOY](https://bridge.joystream.org/transfers/0-18) tokens them from the Marketing WG budget and bridged it to the EthAdmin multisig on Base Network. This transfer was made to provide deeper liquidity for the Joystream/USDC trading pair and adding LP transaction was [executed](https://app.safe.global/transactions/tx?safe=base:0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747&id=multisig_0x62e6849aBA4Da5647374E41Bafb3f40588Ab4747_0x3ab0c13b4e36e686f72c0641e0daba236ed24d796afd76042d84f07c0b0d1e11) by signers.
- Infrastructure assurance payments were sent on Ethereum mainnet, [reported on Pioneer](https://pioneerapp.xyz/#/forum/thread/890?post=7080) and discord. There were discussions with the Infrastructure Lead about the feasibility of some expensive nodes at the beginning of the term. The Council expects some DP servers to shut down in Term 39.

### Proposals: [https://pioneerapp.xyz/#/council/past-councils/00000011](https://pioneerapp.xyz/#/council/past-councils/00000011)

## **7. Financial**

**Overall Spending**

| Item | Spending (previous term), JOY | Spending (current term), JOY |
| --- | --- | --- |
| Council rewards | 933,333.333 | 933,333.333 |
| WG filled | 1,833,186.384 | 1,086,936.403 |
| Funding proposals | 262,054 | 61,820 |
| Validator rewards | 1,201,365 | 1,190,882 |
| Grand Total | 4,229,938.717 | 3,272,971.736  |

**WGs’ Spending**

| Working group | Spending (previous term), JOY | Spending (current term), JOY |
| --- | --- | --- |
| Builders | 155,500 | 0.002 |
| Storage | 312,966.733 | 165,286.97 |
| Distribution | 0.012 | 137,293.041 |
| Content | - | - |
| HR | 363,999.97 | 203,866.64 |
| Marketing | 1,000,719.669 | 580,489.749 |
| Total | 1,833,186.384 | 1,086,936.403 |

*Note: The Content WG appears to have no spending because the working group lacks a lead, who is the only one capable of paying workers from the WG budget. As a workaround, workers were paid through a series of funding proposals. This term, the BWG has not executed salary payments. This is because the lead is new and occupied with other responsibilities.
***
Chart 7.1. WGs’ spending for current term, JOY**

![image.png](Council%20Report%20Term%2038/image.png)

**Chart 7.2. WGs’ spending (current term VS prev term), JOY**

![image.png](Council%20Report%20Term%2038/image%201.png)