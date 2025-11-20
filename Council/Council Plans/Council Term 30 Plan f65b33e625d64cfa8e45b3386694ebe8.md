# Council Term 30 Plan

- Dates:  27 Feb 2024 → 12 March 2024
- Council Term: 30
- Start block: `6,393,629`
- End block: `6,477,350`

## 1. Composition

- leet_joy, 31%
- dmtrmltsv, 21%
- tomato, 21%

Election results: [https://pioneerapp.xyz/#/election/past-elections/0000000u](https://pioneerapp.xyz/#/election/past-elections/0000000u)

## 2. Previous Council's Recommendations

- Issues to address
    - Research and fix the issue with failed uploads.
- Budgeting and Salary Model
    - Create a budgeting tool for modeling different scenarios for Q1.
    - Set up a process for vesting payments, including manage=ment and recording of these payments.
    - Adjust the salary model based on actual needs and outcomes from the pilot of the current salary model.
    - Consider developing a model for council salaries.
- WG
    - Progress on the ongoing consolidation of SWG and DWG.
    - Decide on the composition of the BWG team in collaboration with BWGL.
- Other
    - Continue validators verification.
    - Vote on the Nara upgrade and Validator set increase.
    - Enforce proposals to find external services for Creator token video and budget modeling assistance.
    - post JDs on external website
    - consider to introduce an OTC process for P2P trades

## 3. Previous Council's Report Feedback

- The council report was not posted on Pioneer as of the 4th of March, 2024 (this is 6 days into the new term) so is quite late. The reasoning for the delay is probably due to a high number of structural changes to the DAO as well as many high priority items taking precedent at the current point in time. The report on Notion was used as the source for this section.
- There are 2 terms (22, 23) that appear to have erroneously high inflation. This appears to be because the membership WG (faucet) funds were not accounted for properly (they are burnt, so the actual figures on these two terms should be lower). It may be necessary to re-review previous terms and update some of the inflation figures based upon this but it is not of critical priority right now.
- Feedback on Actions suggested by previous council: basically all of the recommendations were approved and agreed upon by the new council.

## 4**. Tasks & OKRs**

### Council tasks

- Set up a process for vesting payments, including management and recording of these payments.
- Work with Klaudiusz to prepare manual on vested
- Review signal proposals for Nara (prev review: [https://pioneerapp.xyz/#/forum/thread/658?post=5139](https://pioneerapp.xyz/#/forum/thread/658?post=5139))
- Research and fix the issue with failed uploads.
- Follow up on `Using Web2 Services By DAO` proposal ([https://pioneerapp.xyz/#/proposals/preview/810](https://pioneerapp.xyz/#/proposals/preview/810)) and also prepare a budget breakdown of web2 services
- Initiate a survey or community call for validators to better understand their incentives as well as start to get them be more proactively involved in the community.
- **Optimize resources across Tech and Non-tech WGs,** including:
    - **DWG/SWG Merger**: To finalize a plan for the SWG and DWG merger. To open an Infrastructure Lead position to assess if we can attract the necessary talent and the cost involved.
    - **HRWG**: Post JDs - establish a process for posting JD on web2 platforms.
    - **CWG Team Revamp**: Streamline CWG operations. Re-assess top tier channels. Fix Gleev homefeed. 
    **CWG:** Draft creator onboarding improvement initiatives and draft creator engagement improvement initiatives.
    - **BWG**: Review budgets versus roadmap items and optimize as necessary. Decide on the composition of the BWG team in collaboration with BWGL.
    - **MWG Reinforcement**: Support MWG in locking down Q1 strategy and budgets, and assist in strengthening the position to execute the marketing strategy.
    - **Membership**: Continue validators verification.
- **Budgeting:**
    - Work with external org to create a budgeting tool that helps model different scenarios over Q1.
    - Do analysis of council budget replenishment after leads are paid on vested terms—is the current replenishment rate enough? (note: this can only be changed after `nara` runtime upgrade actually executes)
    - Create representation of vested payments within budget spreadsheet
        - is it worth building a custom tool for this?
        - is the “treasury team” capable of producing spreadsheets/models for this?
- **OKRs Adoption**: Assist with syncing on OKRs progress.

### Builders WG

1. Help SWG&DWG fully roll out squid-based nodes.
2. Continue work on Luxor runtime upgrade, prepare a document with a full scope.
3. Continue Nara upgrade operations and ensure smooth upgrade.
4. Start R&D for Argo Ethereum bridge.
5. Deliver WalletConnect support in Atlas.
6. Find a solution to QN availability issues.

### Distribution WG

1. Start consolidation of Storage workers into Distribution Worker (starting from DWGL node)
2. Continuing on enriching Elastic search dashboard with RUM data (small issues on the logs need to be fixed)
3. Argus 2.0 Deployment on DWGL node
4. Possibly Argus 2.0 release

### Storage WG

- **Implement the Council's proposed reorganization model for the WG.**
- Develop a detailed plan for the DWG + SWG merge, which will include:
    - Identifying the geographies based on the sessions registered by the distributor.
    - Reducing the total headcount of DWG and SWG by having most operators run both nodes
    - Exploring further reduction of the replication factor, subject to an acceptable level of data object loss
    - Exploring a deep-freeze layer for storage.
    - Relocating the servers to clusters closer to the geographies with the highest sessions, as well as optimizing locations within current geographies (taking the lead on this but in collaboration with Mr. Bovo)
    - Noting that most of the sessions we have are coming to the homepage and scrolling a few pages down, so distributor nodes mostly have it cached. This should be taken into consideration when choosing the requirements for the storage machines. Review if we actually need the fast and expensive machines. Incorporate to cost cutting plan.

*REMARK: the entire plan execution is attainable within the current term but detailed timeline and cost impact on overall infra is expected to be presented by SWG by the end of this term.*

### Marketing WG

**KR-4.8 [Marketing] Achieve a 20% increase in total social media impressions compared to the previous quarter**

- Hire additional workers to enhance the capacity of the working group.
- Social media content management:
Create content for social media posts and forum announcements/updates
Publish weekly summary on Joystream blog
Support product launches (Dashboard, Validator page) & events (Fireside chat)
Prepare graphic assets and content for TOP3 weekly channels, and post it on Twitter
Update socials with content
Organize NARA / CRT twitter spaces
- Create a community-driven campaign for content creation, including infographics and memes

**KR-4.5 [Marketing] Onboard 10 Marketing Ambassadors**

- Ambassador program promotion and management (high priority)

**KR-4.4 [Marketing] Reach 32,000 non-empty channels and 1,400,000 non-spam videos on Joystream by the end of Q1**

- Execute a video production and publishing campaign that highlights the YPP program on popular YouTube channels, aimed at boosting creator growth. (high priority)
- Share creators success stories on blog / socials

**KR-4.3 [Marketing] At least 3 new interviews with Joystream team are conducted and published**

- Reach out to potential KOLs who will be hosting AMA sessions with JoyStream
- Start an advertising campaign on YT for uploaded interview video

**KR-4.2 [Marketing] At least 25 new Joystream-related review videos targeted at crypto audiences are posted on Youtube**

- Outreach to crypto creators

Other tasks:

- **CRT campaign** - outreach to youtubers who will mint and promote CRT (high priority)
- **Come up with a campaign calendar for each marketing channel** (high priority)
- **CMC communities campaign** (high priority)
- Marketing proposals
- Update coin trackers
- Fireside chat highlights (create videos for X)

### Human Resources WG

- **JD posting and hiring process / setup Breezy platform when it’s available**
- Execute 1 or more Community Events in Term 30
- Prepare Weekly Roundups
- Moderate DAO-Daily Standup and main governance meetings
- Community support

**Forum worker (part of HRWG)**

- Create needed new categories/subcategories on the forum
- Archive inactive, closed, or concluded threads

**Membership worker  (part of HRWG)**

- Keep faucet replenished
- Monitor faucet use
- Verify Validators > aim to do at least 1/3

### Content WG

- **Gleev homepage**
- Homepage feed update with top 50 videos
- Homepage feed update with channel by weights in coordination with
JSG (reranking of current channels with tiers as part of this task)

Creator engagement:

- Shortlist new candidates for Creator Fireside Chat
- Review Creator Onboarding flow and suggest improvements to drive engagement
- Review incentives for unique content creation and suggest improvements
- Re-Implement Creator engagement analytics tools
- Work towards Creator Advisory panel composition
- Work with Robert on creating CRT onboarding video

Ongoing operations:

- Creator support via email, discord and github (email access still required for Richard and dmtrmltsv, depends on JSG team)
- YPP reports to be done every Sunday (requires timestamp for Hubspot feed to be updated, depends on JSG team)

Team ops:

- Hire Igrex as deputy
- Review the structure of timesheets for ad-hoc and per hour compensation

## **5. Budget**

EMA30 price: **0.022**

**Council budget**

| Item | JOY | USD-EMA30 |
| --- | --- | --- |
| Start budget | 14,176,861.86 | 311,890.96 |
| Spending (planned) | **1,659,887,7** | 36,517.52 |
| Refill (planned) | **1,465,000** | 32,230 |
| End budget (planned) | 15,211,851.86 | 334,660.74 |

Start USDT treasury:  

### **Inflation**

- Planned inflation for the term: 0.248%
- Projected inflation this year: 5.952%

(if all remaining periods had same issuance as the current one)

| Term | Minted, MJOY | Inflation |
| --- | --- | --- |
| 1 | 0.453 | 0.045% |
| 2 | 0.909 | 0.091% |
| 3 | 3.056 | 0.306% |
| 4 | 1.274 | 0.127% |
| 5 | 1.414 | 0.141% |
| 6 | 1.822 | 0.182% |
| 7 | 1.491 | 0.149% |
| 8 | 1.451 | 0.145% |
| 9 | 1.666 | 0.167% |
| 10 | 1.329 | 0.133% |
| 11 | 1.313 | 0.131% |
| 12 | 2.087 | 0.209% |
| 13 | 2.013 | 0.201% |
| 14 | 1.575 | 0.158% |
| 15 | 1.834 | 0.183% |
| 16 | 2.157 | 0.216% |
| 17 | 1.677 | 0.168% |
| 18 | 1.761 | 0.176% |
| 19 | 1.642 | 0.164% |
| 20 | 1.648 | 0.165% |
| 21 | 1.744 | 0.174% |
| 22 | 2.477 | 0.248% |
| 23 | 2.517 | 0.252% |
| 24 | 1.666 | 0.167% |
| 25 | 1.776 | 0.178% |
| 26 | 1.476 | 0.148% |
| 27 | 1.460 | 0.146% |
| 28 | 1.576 | 0.158% |
| 29 | 1.839 | 0.184% |
| 30 | 2.47 | 0.248% |
| **Total** | 51.57 | 5.158% |

### **Overall**

EMA30 = 0.022

**Table 5.1. Overall budget**

| **Table 5.1. Overall budget** |  |  |
| --- | --- | --- |
| **Item** | **Spending (planned), JOY** | **Spending (planned), USD-EMA30** |
| Council rewards | 250,000 | 5,500 |
| WG spending, incl: | **1,659,887,7** | 36,517.52 |
| Funding proposals |  |  |
| Creator payout rewards |  |  |
| Validator rewards | 562,000 | 12,364 |
| **Term issuance, Gross** | 2,471,887.7 |  |
| Fees and commissions | 200,000 | 4,400 |
| *1-year vesting | 329,590.73 | 7,250.99 |
| **2-year vesting | 381,817.45 | 8,399.98 |
| **Term issuance, Net** | 1,560,479.52 | 34,330.54 |

### **Working groups**

**Table 5.2. Working groups, JOY budget**

| **Working group** | **Start budget, JOY** | **Total refill (planned), JOY** | **Total spending (planned), JOY** | **End budget (planned), JOY** |
| --- | --- | --- | --- | --- |
| Builders | 19,677.45 | 440,000 | 448,409.09 | 11,268.36 |
| Storage | 70,616.89 | 100,000 | 165,500.00 | 5,116.89 |
| Distribution | 7,778.93 | 105,000 | 110,681.82 | 5,375.29 |
| Forum | 1,015.95 |  | NA | 1,015.95 |
| Apps |  |  | NA |  |
| Content | 9,986.42 | 200,000 | 208,636 | 1,350.42 |
| HR | 25,412.90 | 70,000 | **85,181.79** | 10,231.11 |
| Membership | 45,314.88 | 200,000 | 200,000 | 45,314.88 |
| Marketing | 96,865.38 | 350,000 | 441,479 | 5,386.38 |
| **Total** | **276,668.81** | **1,465,000** | **1,659,887,7** | **81,781.11** |
| *1-year vesting |  |  | 329,590.73 |  |
| **2-year vesting |  |  | 381,817.45 |  |
| Total JOY will be paid with vesting schedule |  |  | 711,408.18 |  |

*1-year vesting: Total 329,590.73
including 227,272.73 (BWG Lead rewards) + 53,000.00 (SWG Lead rewards) + 49,318.00 (DWG Lead rewards)

**2-year vesting: Total 381,817.45
including 163,636 (CWG Lead rewards) + 163,636 (MWG Lead rewards) + 54,545.45 (HRWG Lead rewards)

**Table 5.3. Working groups, USD-EMA30 budget (EMA30 = 0.022)**

| **Working group** | **Start budget, USD-EMA30** | **Total refill (planned), USD-EMA30** | **Total spending (planned), USD-EMA30** | **End budget (planned), USD-EMA30** |
| --- | --- | --- | --- | --- |
| Builders | 432.9 | 9680 | 9864.99 | 247.9 |
| Storage | 1553.57 | 2200 | 3641 | 112.57 |
| Distribution | 171.13 | 2310 | 2435 | 46.13 |
| Forum | 22.35 | 0 | 0 | 22.35 |
| Apps | 0 | 0 | 0 | 0 |
| Content | 219.7 | 4400 | 4589.99 | 29.7 |
| HR | 559.08 | 1540 | 1873.99 | 225.08 |
| Membership (Faucet refill) | 996.92 | 4400 | 4400 | 996.92 |
| Marketing | 2131.03 | 7700 | 9712.53 | 118.5 |
| **Total** | **6086.71** | **32230** | **36517.52** | **1799.18** |
| *1-year vesting |  |  | 7,250 |  |
| **2-year vesting |  |  | 8,399 |  |
| Total JOY will be paid with vesting schedule |  |  | 15,650 |  |