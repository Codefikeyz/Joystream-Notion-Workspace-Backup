# Council Report Term 39

Date: August 29, 2024 → September 27, 2024
Council Term: 39
Testnet / Mainnet: Mainnet

## Council Report

- Dates: 25 October 2024 → 22 November 2024
- Council Term: 00000013
- Start block: 9,835,230 0x9807d08b7abc82241435effdad39ec87004ec442b21f683d54d4664bfb28662e
- End block: 10,238,430 0x1db4e1dd44f322f97d46eefebc58c9af1f1fe38194a6b68afd317db467319930

## 1. Composition

- **leet_joy**, 53% - Chief CM
- **marat_mu**, 3%
- **0x2bc**, 1%

Election results: [https://pioneerapp.xyz/#/election/past-elections/00000013](https://pioneerapp.xyz/#/election/past-elections/00000013)

## 2. General stats

- Channels: **110** (total **30,010**)
- Videos: **4,100** (total **1,427,847**)
- Forum threads: **6** (total **1,003**)
- Forum posts: **34** (total **7,117**)
- Proposals: **11** (total **1,042**)
- Memberships: **512** (total **66,112**)

## 3**. Term Highlights**

- The YPP program was temporarily paused until all critical issues are resolved; new sign-ups were disabled and landing/studio pages were updated accordingly (new designs were prepared by Magda and landing/studio pages were updated).
- Builders achieved a significant (10x) improvement with YT-sync speed.
- Creator Token [Marketplace page](https://gleev.xyz/crt-marketplace?currentPage=0&perPage=10&orderBy=liquidity_DESC) was updated and listing issues were fixed (see related [Gleev](https://github.com/Joystream/gleev/pull/67) and [Orion](https://github.com/Joystream/orion/pull/348) PR's)
- Opted-out channels (12,494 channels affected by opt-out bug (expired API token)) from [https://github.com/Joystream/youtube-synch/issues/337](https://github.com/Joystream/youtube-synch/issues/337) will require creators to manually sign in on Gleev again, which will be announced once all YT-sync issues are resolved.
- An archive script was developed and tested by BWG, and the Infrastructure lead started the library sync process, 10 TB of data has been transferred to S3 so far. It may take about 2 months until the data is transferred fully.
- This term's chief council experiment continues, with all three winning election candidates adhering to the agreed-upon structure.
- The Council decided to burn 5M JOY of the council budget ([https://pioneerapp.xyz/#/proposals/preview/1042](https://pioneerapp.xyz/#/proposals/preview/1042)) to reduce unnecessary risks.
- [Colossus: Rework sync and cleanup](https://github.com/Joystream/joystream/pull/5194)

## 4**. Tasks Status**

**YT-sync and YPP Status Summary:**

Program Status:

- YPP program was [paused](https://pioneerapp.xyz/#/proposals/preview/1033) until all critical issues are resolved
- New designs were prepared by Magda and landing/studio pages were updated
- New sign-ups were disabled

Sync Performance:

- Speed improved from 200 to 2000 videos/day using IVPN proxies
- Further scaling possible with additional proxy servers
- The syncing queue is slowly dropping

YPP Issues:

- 12,494 channels affected by opt-out bug (expired API token)
- Most valuable channels (479 with high weights) currently opted-out
- To avoid it further is recommended to develop and maintain a script that will use creators API tokens once per XX days (this would not be required if we will not switch from ysing yt-dl)

Recovery Plan:

- Re-enabling YPP sign-ups after processing current sync queue
- Adding re-sign-up button in Gleev studio
- Planning email outreach to opted-out creators
- Implementing automatic verification for affected channels

**CDN Optimization & Archive Script Status**

- Archive Script was developed by Lezek, it was also updated to not rely on separate bucket
- It was tested by Infrastructure working group and started sync
- Current storage stats: ~10 TB synced to archive, total Joystream content ~100 TB

**BASE ecosystem** 

- We engaged with the Aerodrome DEX team but they indicated our metrics were insufficient for a partnership. With only 100 token holders on Base network, they suggested revisiting once we achieve higher daily trading volumes.
- MWG & ambassadors listed JoystreamERC20 on multiple websites increasing reach.
- The AMM on Uniswap remains untouched, and it is highly recommended to bridge more JOY to the EthAdmin multisig in Term 40.

**Operational Tasks** 

- Processed regular proposals & hiring (created new opening for Joystream CMO)
- Maintained council/working groups communication
- Facilitated USDT server compensation for CDN workers
- Handled routine governance matters

## 5**. WGs’ Status**

**Legends**:
*🟢 Completed*

*🟡 Started but not completed / WIP*

*🔴 No work was done or not achieved*

### **Builders WG**

Lead: Lezek

[Plan](https://pioneerapp.xyz/#/forum/thread/62?post=7057) - [Report](https://pioneerapp.xyz/#/forum/thread/62?page=4)

**🟢 Atlas CRT listing issues:** The CRT listing issues were fixed, see related [Gleev](https://github.com/Joystream/gleev/pull/67) and [Orion](https://github.com/Joystream/orion/pull/348) PR's

**🟡 Colossus cleanup issues:** Because some cleanup issues were still experienced by *@mmx1916*, I decided to rework Colossus to limit resource usage (especially memory) during sync and cleanup ([related PR](https://github.com/Joystream/joystream/pull/5194)). Once the PR is merged the status of the issue needs to be verified again.

**🟡 Archive script:** Archive script is finished and currently being executed by *@freakstatic* Almost 10 TB of data has been transferred to S3 so far. It may take about 2 months until the data is transferred fully.

- **Task 1:** Continue supporting *@freakstatic* in case any technical issues w/ the archive script arise.
- **Task 2:** Add features to Storage CLI that will simplify removing / adjusting large buckets in order to reduce replication rate after the archive is fully set up.

**🟡 Fixing YPP / YouTube sync:**

- YPP was temporarily paused
- It was possible to address the syncing issues by adjusting the proxy setup for Youtube Sync. Currently we're syncing ~2000 videos daily,
which is ~10x more than before, the syncing queue is slowly dropping.
- **Task 1:** Re-enable YPP sign-ups and, update the message displayed in YPP dashboard, so that opted-out creators can join again.
- **Task 2:** Add a *List* of creators that were affected by the [opted-out issue](https://github.com/Joystream/youtube-synch/issues/337) to HubSpot to allow targeting them with a dedicated e-mail campaign.
- **Task 3:** Verify payment status of YPP creators and restore YPP payments.

**🟡 Planning:** [Joystream technical issues](https://docs.google.com/spreadsheets/d/1OGxo8ranpirLSjWFbLh-rmqgaU0Q9wGGN8oox4D5q1c/edit?gid=0#gid=0) spreadsheet still needs to be updated and re-evaluated

### **Storage WG**

Lead: Freakstatic

[Plan](https://pioneerapp.xyz/#/forum/thread/879?post=7061) - Report (WIP)

**🟢** Maintain a replication rate of not lower 2 for all objects.

**🟢** Maintain percentage of unaccepted objects < 2%.

**🟢** Maintain percentage of lost objects 0%.

**🟢** Maintain a storage system availability of 100%

*Note: Smooth operations, some workers are in the process of migrating to a cheaper server. Workers were paid with USDT on Ethereum for their servers.*

### **Distribution WG**

Lead: Freakstatic

[Plan](https://pioneerapp.xyz/#/forum/thread/85?post=7055) - Report (WIP)

**🟢** Monitoring

**🟡** Migrate @Deathix node to a cheaper server to reduce costs

### **HR WG**

Lead: **Codefikeyz**

[Plan](https://pioneerapp.xyz/#/forum/thread/119?post=7043) - [Report](https://pioneerapp.xyz/#/forum/thread/108?post=7082) 

*🟢* Information Dissemination including council election facilitation, daily updates postings and EMA30 value announcement

*🟢* Publication of Weekly Summary

*🟢* Meetings and engagement coordination and moderation

*🟢* Discord and Faucet Management

### **Content WG**

Lead: NA

*🟢* Content Moderation across all homepage feed categories and marketplaces

*🟢* YPP program support for verification (first 2 weeks of the Term)

### **Marketing WG**

Lead: **leet_joy**

[Plan](https://pioneerapp.xyz/#/forum/thread/68?post=7045) - [Report](https://pioneerapp.xyz/#/forum/thread/46?post=7129)

*🟢* Ambassador program promotion and management

6 ambassadors were excluded from the program;

MWG is preparing to announce its next phase in December.

*🟡* Social media content management

We have started looking for professional marketing content creation studios offering subscription-based plans and plan to hire one to enhance our content quality and overall content strategy.

*🟢* CMC communities campaign

With significant progress by our builders on re-enabling YT-sync, MWG is working on enhancing our strategy for CMC. We are preparing accounts and instruments for effective campaigns. The MWG is also promoting Joystream-related posts (eg. [~100K impressions](https://coinmarketcap.com/community/post/342479640/)) on CMC using own affiliate accounts.

*🟢* Listings of wrapped JOY

A significant amount of work was put into listing our BASE asset on various platforms.

*🟢* Listing of wrapped JOY on Aerodrome DEX

MWG engaged with the Aerodrome team and received a response to our application. In short - we will be listed when our traction numbers on the BASE chain become more favorable.

*🟢* Atlas CRT listing issues

MWG worked with Builders ([Gleev](https://github.com/Joystream/gleev/pull/67) and [Orion](https://github.com/Joystream/orion/pull/348) PR’s) to improve CRT marketplace page.

## 6**. Budget**

### **Overview**

- Starting Council budget: **16,644,320.203 JOY**
- Spending from Council budget: **2,133,333.333 JOY**
- Refill of Council budget: **4,667,600 JOY**
- Ending Council budget: **14,178,586.87 JOY**

**Other Assets**

- [SAFE](https://pioneerapp.xyz/#/proposals/preview/497) (Ethereum mainnet):  6,378.50 USDT
- [ETHAdmin](https://pioneerapp.xyz/#/proposals/preview/961) (BASE): Uniswap Liquidity NFTs ****~$19.91K USDC
- DAO VCC: 1,450.46 USDT

**Inflation**

- Start issuance: **1,087,137,898.65 JOY + 7,072,559 JOY** ([base network](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c))
- End issuance: **1,088,726,603.341 JOY + 8,703,024 JOY** ([base network](https://basescan.org/token/0x8761155c814c807cd3ccd15b256d69d3c10f198c))
- Term issuance: **3,219,169.69 JOY** (L1 issuance: 1,588,704.691 JOY and BASE network issuance: 1,630,465 JOY)
- Term issuance: **0.321 %**
- JOY burned (bridged to other chains): **1,630,465** JOY
- JOY burned (fees and commissions): **86,823.741 JOY**

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
| 36 | 6.480 | 0.648% |
| 37 | 3.683 | 0.368 % |
| 38 | 3.272 | 0.327% |
| 39 | 3.321 | 0.321% |
| **Total**  | 97.42 | 9.742% |

**Table 6.2. Overall Budget**

| **Item** | **Total spending (planned), JOY** | **Total spending (actual), JOY** |
| --- | --- | --- |
| Council rewards | 933,333.00 | 933,333.333 |
| WG spending, incl: | 1,808,936.40 | 1,183,704.098 |
| Funding proposals | 65,000 | 0 |
| Validator rewards | 1,200,000.00 | 1,188,956 |
| Term issuance, Gross | 4,007,269.40 | 3,305,993.431 |
| Tokens bured | (150,000.00) | (1,717,288.741) |
| Term issuance, Net | 3,857,269.40 |  1,588,704.69 |

*Notes: DWG, CWG, HRWG and BWG have not paid salaries for some workers. Tokens burned also includes a number of  1,630,465 JOY bridged to BASE chain. 2598,52 USDT [was spent](https://pioneerapp.xyz/#/forum/thread/890?post=7123) from the DAO SAFE for maintaining the infrastructure.*

**Table 6.3. WGs’ Workers**

| Working group | Workers number (incl Lead) | Workers hired | Workers fired | Workers left |
| --- | --- | --- | --- | --- |
| Builders | 2 | 0 | 0 | 0 |
| Storage | 6 | 0 | 1 | 0 |
| Distribution | 7 | 0 | 1 | 0 |
| Forum | 1 | 0 | 0 | 0 |
| Apps | 0 | 0 | 0 | 0 |
| Content | 2 | 0 | 0 | 0 |
| HR | 5 | 0 | 0 | 0 |
| Membership | 0 | 0 | 0 | 0 |
| Marketing | 5 | 0 | 0 | 0 |
| Total | 28 | 0 | 2 | 0 |

### **Table 6.4. WGs’ Budgets, JOY**

| **Working group** | **Start budget, JOY** | **Refilled, JOY** | **Spending (planned), JOY** | **Spending (actual), JOY** | **End budget, JOY** |
| --- | --- | --- | --- | --- | --- |
| Builders | 554,887.093 | 600,000 | 622,000 | 0.004 | 1,154,887.089 |
| Storage | 71,746.297 | 200,000 | 165,286.97 | 271,746.297 | 0 |
| Distribution | 281,723.618 | 0 | 137,293.041 | 215,906.377 | 65,817.241 |
| Forum | 1,015.952 | 0 | 0 | 0 | 1,015.952 |
| Apps | 0 | 0 | 0 | 0 | 0 |
| Content | 6,433.419 | 0 | 0 | 0 | 6,433.419 |
| HR | 4,565.953 | 200,000 | 203,866.64 | 52,666.67 | 151,899.283 |
| Membership | 0 | 0 | 0 | 0 | 0 |
| Marketing | 508,346.792 | 200,000 | 680,489.749 | 643,384.749 | 64,962.043 |
| Total | 1,428,719.125 | 1,200,000 | 1,808,936.40 | 1,183,704.098 | 1,445,015.027 |

Notes:

- For a full breakdown of each working group's expenses, refer to Section 5. Each working group's status includes a link to the lead's report.
- Stablecoin spending includes $150 for Magda's Gleev designs, $60 for the Typeform plan, and $2,598.50 for infrastructure payments.
- The column titled `Spending (actual), JOY` represents the actual amounts spent by each working group, primarily on salaries. For the Marketing WG, this also covers various initiatives.
- This term, the BWG has not executed salary payments. This is because the lead is new and occupied with other responsibilities.
- Most salaries in the working groups are USD-denominated and subject to vesting schedules (determined at the beginning of each term) and an EMA30 limit, which was implemented this term. Consequently, the salaries do not reflect the current token price as they are affected by the EMA30 cap and vesting.
- Infrastructure assurance payments were sent on Ethereum mainnet, [reported on Pioneer](https://pioneerapp.xyz/#/forum/thread/890?post=7080) and discord. There were discussions with the Infrastructure Lead about the feasibility of some expensive nodes at the beginning of the term.

### Proposals: [https://pioneerapp.xyz/#/council/past-councils/00000013](https://pioneerapp.xyz/#/council/past-councils/00000013)

## **7. Financial**

**Overall Spending**

| Item | Spending (previous term), JOY | Spending (current term), JOY |
| --- | --- | --- |
| Council rewards | 933,333.333 | 933,333.333 |
| WG filled | 1,086,936.403 | 1,183,704.098 |
| Funding proposals | 61,820 | 0 |
| Validator rewards | 1,190,882 | 1,188,956 |
| Grand Total | 3,272,971.736 | 3,305,993.431 |

**Chart 7.1. Overall spending for current term, USDT’**

![image.png](Council%20Report%20Term%2039/image.png)

**Chart 7.2. Overall spending (current term VS prev term), JOY**

![image.png](Council%20Report%20Term%2039/image%201.png)

**WGs’ Spending**

| **Working group** | **Spending (previous term), JOY** | **Spending (current term), JOY** |
| --- | --- | --- |
| Builders | 0.002 | 0.004 |
| Storage | 165,286.97 | 271,746.297 |
| Distribution | 137,293.041 | 215,906.377 |
| Content | 0 | 0 |
| HR | 203,866.64 | 52,666.67 |
| Marketing | 580,489.749 | 643,384.749 |
| Total | 1,086,936.403 | 1,183,704.098 |

*Notes: DWG, CWG, HRWG and BWG have not paid salaries for some workers.*