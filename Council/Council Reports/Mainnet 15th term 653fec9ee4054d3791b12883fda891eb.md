# Mainnet 15th term

Date: July 18, 2023 → August 1, 2023
Council Term: 15
Council Terms: 15 (https://www.notion.so/15-2a72053e1d60439aa084bf691c112931?pvs=21)
Testnet / Mainnet: Mainnet

# Council Report - Term #15

[Council Term #15 Plan](https://pioneerapp.xyz/#/proposals/preview/417)

**Composition:**

- 0x2bc
- leet_joy
- l1dev

→ [election result](https://pioneerapp.xyz/#/election/past-elections/0000000d)

**Term boundaries:**

- Start block: `3153614`

`0x17b6c120420d1754757b197b7bbb8cef1b9243008fca333118339b12c048ebe3`

- End block: `3369615`

`0x0437df96c9042e26d54acff9a2c0319e7464c5a04227343692cf3b5304e24885`

## 1. General stats

- Channels created: `206` ****(`26798` total)
- Videos: `11915` (`50001` total)
- Storage Capacity Used:  **`xxx`** GB
- Forum categories: `57`
- Forum threads: `24` (`504` total)
- Forum posts: `135` (`4299` total)
- Proposals: `27` (`22` executed)
- Memberships: `396` (`7688` total)
- Available WG budgets:  `0.3`  mJOY
- Available Council budget: `56.5` mJOY
- Total WG Openings: `117`
- Total WG Applications: `173`
- Total Filled positions
    - Workers hired: `4`
    - Workers fired: `1`
    - Workers left: `0`

## 2. Summary

- The Gleev team released a major update for Joystream. Introducing user accounts on the server side (Orion) and enabling sign-up with email and password (aka custodial wallets on Atlas). New members can now easily create accounts with email and password, eliminating the need to sign every transaction with the signer.
- [Council Overall Spending Dashboard](https://dapplooker.com/dashboard/joystream-council-overall-spending-dashboard-355) and [Working Group Spending Dashboard](https://dapplooker.com/dashboard/joystream-working-group-spending-dashboard-356) developed by Dapplooker. It shows council spending across all working groups during the entire mainnet period.
- JOY markets indicated a significant increase in volume and price.
- Surge in video uploads.
- YT-sync was manually disabled by JSG due to overload. YT-sync will be accepted manually by JSG.
- Channel with video-games video was synced and get 15+ TB of our storage triggering discussions and executing limitations on YT-sync based on Tiers.
- A proposal [424](https://pioneerapp.xyz/#/proposals/preview/424) to grant @tomato Discord server admin rights passed and he was promoted by JSG to perform this role.
- A proposal [419](https://pioneerapp.xyz/#/proposals/preview/419) to grant @leet_joy access to posting under @JoystreamDAO Twitter account passed and he got the necessary access to TweetDeck and Buffer.
- Joystream organization profile was approved by DeBank and MWG managed to promote it’s grow to top 35 platform profiles with 5K followers in less than a week.
- DWG lead replacement, Mokhtar will take vacation until end of August and bwhm will perform in this role during this period.
- Friday Fireside chat took place on Twitter Spaces.
- Sunday Townhall meeting took place on Discord where JSG shared a presentation of a recent Atlas update. Unfortunately, the video was not recorded by the HRWG.
- DAO Weekly quiz was held by HRWG on Discord.
- OKR Q3 was [approved](https://pioneerapp.xyz/#/proposals/preview/410).
- The membership fee was [increased](https://pioneerapp.xyz/#/proposals/preview/428) to 50 JOY to avoid possible abuse.

## 3. Tasks Status

### Council tasks

**OKR & WG performance**

- 🟡Final assessment of Q2 OKRs achievement
- 🟢Approve Q3 OKRs
- 🟡Approve DAO roadmap
- 🟢Define [OKR life cycle](https://pioneerapp.xyz/#/proposals/preview/189)
- 🟢Review WG plans, reports, communicate new tasks and follow-up, remind if necessary.

**Maintain Network Security**

- 🟢Collect new volunteer SP/DP Validating nodes stashes and ask community to stake to these nodes
- 🟢YPP adoption: The number of bew YPP participants per term should increase by 10%

**Recruiting**

- 🟡Hire Membership Lead - opening canceled.
- 🟡Hire Council Secretary - opening canceled.

### AWG

- 🔴Publish a strategy to increase the adoption and profitability of existing Apps.
    - 🟡DAO-wide YPP: test deploy YPP backend, develop reward scheme
    - 🟢Joyspace DAO Gateway: Carry out logo competition (@codefi)
- 🟡Publish a realistic development roadmap to attract new audiences (topics, devices).
    - 🟢Publish weekly bounty updates to the wider community.
    - 🟢Regularly add more development bounties.
    - 🟡Formalize the application, oracle selection, review and payment process.
- 🔴 [CR documentation](https://github.com/Joystream/community-repo): create Apps page to attract developers, summarize / reference GH issues
- 🟢Storage SDK API: [continue research](https://pioneerapp.xyz/#/forum/thread/47?post=3960) with SWG/DWG leads to clarify specifications
- 🔴[Organize workshops](https://pioneerapp.xyz/#/forum/thread/300): write documentation on existing tools as base for future workshops held by HR+ /   *[PR to improve documentation](https://github.com/Joystream/orion/pull/152).*
    - 🔴Conduct a training session about Gateways (*can be turned into a bounty)*
    - 🟡Suggest a reward model to attract and motivate long-term operators.

### BWG

**top priority**

- 🟢 Validator Page ([Validator Page Dev](https://github.com/Joystream/pioneer/issues/4321)) - push to production

**other priority**

- 🟢 Discord Role Bot - submit PR
- 🟡Calamar Explorer Update -  submit PR
- 🟡Pioneer Backend MVP ([Email Notifications](https://github.com/Joystream/pioneer/issues/4230)) - submit PR
- 🟢DappLooker dashboard - keep maintaining

### CWG

- 🟢Collect best performing channels and submit Creator Payouts proposal.
- 🟢The main work of curating videos, channels and metadata (resources) in [Gleev](https://gleev.xyz/) and [l1.media](https://l1.media/)
- 🟢All non yt-synch channels are reviewed for Reward Content Policy by curators in more than 48 hours after first video is published [objectives score [OKR](https://miro.com/app/board/uXjVMaVGcaY=/)]

### DWG  - no report

- Migrate all operators to deploy distributor node with docker, using latest published images: allowing easy migration to newer versions, or rolling-back as necessary. Update relevant guides in notion.
- Update query-node instances to also use latest image, (mind the major db version change) - for better performance Postgres14 + node version 18.
- Update query.joystream.org QN with metrics to assess general QN issues
- Assess request flow for playing videos, identify latency points and implement solution.
- Deploy new versions of distributor node and storage nodes with open-telemetry metrics once PR is merged.
- Add OS metrics for distributor nodes to monitoring dashboard.(MetricsBeat)
- Start work on adding prometheus metrics to DP/SP nodes to addd to monitoring capability.
- Work with Atlas team to deploy new monitoring/stats/logging once ready.
- Write/Update cli tool to fetch assets - use Gleev code, query and fetch mechanism.
- Write/Update cli tool to bench QN (use ‘slow’ queries)

### FWG

- 🟢Review pre-proposal threads, remind participants and archive if necessary
- 🟢Reward best forum thread for the term
- 🟢Post 1 community guide on Forum

### MWG

**top priority**

- 🟢Focus on support of JOY value incl. marketing and growth of key product metrics
- 🟢Ensure adequate funding for marketing activities.
- 🟢Ensure progress towards listing on better exchanges.
- 🟢Research on existing Ambassador Programs.
- 🟡Develop Ambassador Program and submit a detailed model in pre-proposal thread.
- 🟢Outreach to content creators on YouTube. Initiate contacts, send js review google forms.

**other priority**

- 🟢Joystream token listing on the additional exchange, schedule necessary calls and ensure we progress towards additional markets for JOY.
- 🟢Increase Joystream presence on web3 platforms. (farcaster, bluesky, bitcointalk.org)
- 🔴Reach top Validators team and communicate to them Joystream validating opportunities
- 🟢Organize at least 3 posts for KOLs about Joystream with a total coverage of at least 10000 views.
- 🟢Promote community Twitter Spaces and Discord events outside of Joystream.
- 🟢Improve usage of content generated by the community.

### SWG

- 🟢Maintain a replication rate of 4
- 🟢Maintain failed upload rate < 5%, investigate and report on failed uploads
- 🟢Publish validator addresses of all workers [on the forum](https://pioneerapp.xyz/#/forum/category/50) for nomination to increase network security.
- 🟡Collaborate with the Subsquid team and actively participate in the Subsquid private testnet.

### HR

- 🟢Research on other communities Discord servers structure, initiate necessary discussions and submit a proposal with list of channels that would be seen to Joystream newcomer.
- 🟢Research on verification procedures done by other Discord communitites, initiate necessary discussions and submit proposal with good solution to Discord Captcha bot.
- 🟢Moderate Discord server efficiently based on Server Rules
    - (1) Make sure that there HR workers check all the channels every 4 hours to delete spam posts.
    - (2) Advise HR workers to check both Discord and TG at the beginning and end of their work
    - (3) Timely announcements and warnings will be done
- 🟢Continue work on Engagements and Documentation
    - (1) Schedule the engagements and workshops
    - (2) Make sure the speakers and agenda are ready a day before the workshop/engagement
    - (3) Document them and publish them in a timely manner
- 🔴Coordination with the leads regarding recruitment and governance matters
    - (1) Coordinate with the leads with the positions they need
    - (2) Make appealing post of the vacancies in the DAO and spread in outside Joystream as well
    - (3) Collect applicants, conduct an initial interview if necessary, and pass to the leads

### Memberships WG

- Keep constant monitoring of the faucet address(es). If we get a large rise in user signups then this needs to be refilled more regularly.
- Keep monitoring of usage of the invitation feature, as this impacts the WG’s budget.
- Ensure the Membership WG budget does not reach 0 as this prevents people from being able to use the invitation feature.

## 4. **Working Groups**

**Table 4.1. Working groups**

| No. | **Working group** | **Lead** | **Plan / Report** | **Summary** |
| --- | --- | --- | --- | --- |
| 1 | Builders | **chaos77** | [Plan](https://pioneerapp.xyz/#/forum/thread/62?post=4236) [Report](https://pioneerapp.xyz/#/forum/thread/15?post=4312) | Validator Page pr merged, Role Bot and Tip Bot are ready for final review & testing, updated Dapplooker dashboard  to most recent term data, new dashboard of channels with the number of videos they have, average length of videos and total file size of videos under construction |
| 2 | Storage | **yyagi** | [Plan](https://pioneerapp.xyz/#/forum/thread/493) [Report](https://pioneerapp.xyz/#/forum/thread/506) | Hired 3 new workers, increased required capacity to 25TB, and requested the rest of the team to upgrade to 25TB. Initiate several discussions on storage scaling. |
| 3 | Distribution | **mokhtar** | NA NA | Smooth operations. |
| 4 | Forum | **songoku** | [Plan](https://pioneerapp.xyz/#/forum/thread/492) [Report](https://pioneerapp.xyz/#/forum/thread/508) | Followed up stale pre-proposal discussions, archived closed or concluded threads, reviewed and moved appropriate forum threads. |
| 5 | Apps | **l1dev** | NA [Report](https://pioneerapp.xyz/#/forum/thread/47?post=4300) |  |
| 6 | Content | **igrex** | [Plan](https://pioneerapp.xyz/#/forum/thread/87?post=4205) [Report](https://pioneerapp.xyz/#/forum/thread/107?post=4322) | The main work of curating videos, channels and metadata (resources) in Gleev and l1.media
All non yt-synch channels are reviewed for Reward Content Policy by curators in more than 48 hours after first video is published. |
| 7 | HR | **abramaria_** | [Plan](https://pioneerapp.xyz/#/forum/thread/119?post=4188) [Report](https://pioneerapp.xyz/#/forum/thread/108?post=4297) | Discord reserch, publish daily news, now we will do this at the same time every day. Held quizzes, maintained databases, and council candidates’ fireside chat was canceled. |
| 8 | Membership | NA | NA NA | Membership fee increased to 50 JOY. |
| 9 | Marketing | **leet_joy** | [Plan](https://pioneerapp.xyz/#/forum/thread/68?post=4244) [Report](https://pioneerapp.xyz/#/forum/thread/46?post=4314) | Outreach to content creators on YouTube. Created official profiles on DeBank and Farcaster. Promoted DeBank profile to 5k followers, promoted community calls, review YPP signups, evalutated YT channels for partnerships, provide feedback on dashboard page, prepare/schedule content for socials. |

## 5. Budget for the Term

### **Overview**

- Starting Council budget: `56 957 680,54` JOY
- Spending from Council budget: `1 190 500,39` JOY
- Refill of Council budget:  `750 000,00` ****JOY
- Ending Council budget:   `56 517 180,16` JOY

**Inflation**

- Inflation for the term:   
  start issuance: `1 021 853 322,57` JOY
  end issuance:  `1 023 687 025,09` JOY
  term issuance:  `1 833 702,52` JOY
  Inflation:  ****`0,183` **%**
- Projected inflation this year:  **3.55%** (projected issuance per year **35.5 M JOY** based on total spending so far interpolated to 24 Council terms annually)

Grand Total Spending 

- Term 1 - `.487` M
- Term 2 - `.487` M
- Term 3 - `3.035` M
- Term 4 - `1.284` M
- Term 5 - `1.344` M
- Term 6 - `1.847` M
- Term 7 - `1.541` M
- Term 8 - `.882` M
- Term 9 - `1.839` M
- Term 10 - `1.472` M
- Term 11 - `1.85` M
- Term 12 - `1.46` M
- Term 13 - `2.28` M
- Term 14 - `1.57` M
- Term 15 - `1.83` M
- Total for Terms 1-15: `23,21` ****M (inflation: `2.32` %)

**Table 5.1. Budget overview**

| **Item** | **Total spending (planned), JOY** | **Total spending (actual), JOY** |
| --- | --- | --- |
| Council rewards | 250 560,00 | 250 560,00 |
| WG ***spent*** | 830 000,00 | 1 129 952,44 |
| Funding proposals | 50 000,00 | 0,00 |
| Creator payout rewards | 0,00 | 0,00 |
| Validator rewards | 500 000,00 | 453 190,08 |
| **Grand Total** | **1 630 560,00** | **1 833 702,52** |

## WG Spending (detailed)

**Table 5.2. WG Spending (detailed)**

- Start block: `3153614` `0x17b6c120420d1754757b197b7bbb8cef1b9243008fca333118339b12c048ebe3`
- End block: `3369615` `0x0437df96c9042e26d54acff9a2c0319e7464c5a04227343692cf3b5304e24885`

| **Working group** | **Start budget, JOY** | **Total refilled, JOY** | **Total spending (planned), JOY** | **Total spending (actual), JOY** | **Spending proposals, JOY** | **Workers rewards (via events), JOY** | **Lead rewards (via events), JOY** | **End budget, JOY** | **Workers number (incl. Lead)** | **Workers hired** | **Workers fired** | **Workers left** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Builders  | 13 595,77 | 117 600,00 | 205 557,72 | 117 557,72 | 80 000,00 | 15 867,72 | 21 690,00 | 13 638,05 | 9 | 0 | 0 | 0 |
| Storage | 54 533,54 | 150 000,00 | 125 194,97 | 137 196,33 | -2,00 | 95 452,43 | 41 745,90 | 67 337,21 | 9 | 3 | 0 | 0 |
| Distribution | 67 943,96 | 170  000,00 | 128  507,29 | 237 943,96 | 198 017,00 | 0,00 | 39 926,96 | 0,00 | 8 | 1 | 1 | 0 |
| Forum | 7 817,06 | 8 960,23 | 16 660,94 | 15 930,50 | 800,00 | 0,00 | 15 130,50 | 846,79 | 1 | 0 | 0 | 0 |
| Apps | 233 391,15 | 0,00 | 61 251,94 | 76 839,95 | 0,00 | 43 893,52 | 32 946,43 | 156 551,20 | 4 | 0 | 0 | 0 |
| Content | 34 067,43 | 99 700,00 | 107 932,57 | 111 617,51 | 15 000,00 | 55 492,01 | 41 125,50 | 22 149,92 | 6 | 0 | 0 | 0 |
| HR  | 13 258,58 | 84 239,00 | 87 540,94 | 88 089,10 | 9 951,10 | 36 898,50 | 41 239,50 | 9 408,48 | 4 | 0 | 0 | 0 |
| Membership | 3 154,82 | 20 000,00 | 10 108,00 | 20 000,00 | 20 000,00 | 0,00 | 0,00 | 3 154,82 | 0 | 0 | 0 | 0 |
| Marketing  | 51 384,64 | 290 000,00 | 331 346,62 | 324 777,37 | 260 711,52 | 22146,2518 | 41919,6 | 16 607,27 | 6 | 0 | 0 | 0 |
| **Total** | **479 146,95** | **940 499,23** | **1 074 100,99** | **1 129 952,44** | **584 477,62** | **269 750,43** | **275 724,39** | **289 693,74** | **47** | **4** | **1** | **0** |

### Proposals

[https://pioneerapp.xyz/#/council/past-councils/0000000f](https://pioneerapp.xyz/#/council/past-councils/0000000f)

## 6. Financial statistics

### Council overall spending

**Chart 6.1. Council overall spending**

| Description | **Total spending (15th term), JOY** |
| --- | --- |
| Council rewards | 250 560,00 |
| WG ***spent*** | 1 129 952,44 |
| Funding proposals | 0,00 |
| Creator payout rewards | 0,00 |
| Validator rewards | 453 190,08 |
| **Grand Total** | **1 833 702,52** |

![](https://i.imgur.com/5gjzLOu.png)

### **Council overall spending “current term VS prev term”**

**Chart 6.2. Council spending (current term VS prev term)**

| **Item** | **Total spending (14th term), JOY** | **Total spending (15th term), JOY** |
| --- | --- | --- |
| Council rewards | 250,560 | 250 560,00 |
| WG ***spent*** | 857,438 | 1 129 952,44 |
| Funding proposals | 40,000 | 0,00 |
| Creator payout rewards | 0 | 0,00 |
| Validator rewards | 427,346 | 453 190,08 |
| Grand Total | 1,575,344 | **1 833 702,52** |

![](https://i.imgur.com/cZAT6Vh.png)

**Working Groups overall spending** 

**Chart 6.3. WGs overall spending (15th term)**

| **Working group** | **Total spending (15th term), JOY** |
| --- | --- |
| Builders  | 117 557,72 |
| Storage | 137 196,33 |
| Distribution | 237 943,96 |
| Forum | 15 930,50 |
| Apps | 76 839,95 |
| Content | 111 617,51 |
| HR (GroupBeta) | 88 089,10 |
| Membership | 20 000,00 |
| Marketing (GroupGamma) | 324 777,37 |
| **Total** | **1 129 952,44** |

![](https://i.imgur.com/iK4OX6J.png)

### **Working Groups’ overall spending**

**Chart 6.4. WGs spending (current term VS prev term)**

| **Working group** | **Total spending (14th term), JOY** | **Total spending (15th term), JOY** |
| --- | --- | --- |
| Builders  | 205,558 | 117 557,72 |
| Storage | 125,195 | 137 196,33 |
| Distribution | 128,507 | 237 943,96 |
| Forum | 16,661 | 15 930,50 |
| Apps | 61,252 | 76 839,95 |
| Content | 107,933 | 111 617,51 |
| HR (GroupBeta) | 87,541 | 88 089,10 |
| Membership | 10,108 | 20 000,00 |
| Marketing (GroupGamma) | 131,347 | 324 777,37 |
| **Total** | **874,101** | **1 129 952,44** |

![](https://i.imgur.com/I4Xbjpw.png)

## 7. Council Daily Reports

Daily reports were not published on Pioneer.

## 8. Recommendations for Next Council

**JOY issuance**

- Reduce unnecessary spendings
- Work on re-balancing council spending across various working groups.

**Marketing**

- Ensure adequate funding for marketing activities. Increase budget if needed.
- Improve JOY markets. Make sure Joystream fulfills the requirements for listing on better exchanges.
- Implement the [Ambassador Program](https://pioneerapp.xyz/#/forum/thread/469). (analyze community input, propose optimal model).
- Improve usage of content generated by the community.
- Increase Joystream presence on web3 platforms.

**Infrastructure**

- Compensation plan. Finalise
- Storage infra scaling. How it should be scaled for increased demand?
- DWG new plan
- Ensure that the DWG/SWG has all the necessary resources to cover server costs and make progress in CDN improvements.

**OKRs**

- Work on Q3 OKRs integration DAO-wise

**Roadmap**

- Develop DAO roadmap - set realistic goals