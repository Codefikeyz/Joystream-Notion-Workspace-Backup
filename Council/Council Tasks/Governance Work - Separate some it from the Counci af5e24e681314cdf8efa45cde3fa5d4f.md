# Governance Work - Separate some it from the Council

Public Notion URL: https://joystream.notion.site/af5e24e681314cdf8efa45cde3fa5d4f
Priority: Medium
Tags: OKRs, Roadmap, council, council secretary, governance, multisig (joystream)
Created time: June 10, 2024 12:05 AM
Owner: tomato
Work Status: In Progress
Governance Status: Pre-proposed
Archive Status: No
Days passed since task created: 527
Threads: Council Rewards + Governance Work - Separate some it from the Council and start paying based upon performance (https://www.notion.so/Council-Rewards-Governance-Work-Separate-some-it-from-the-Council-and-start-paying-based-upon-pe-79883b91be8e48ef90831d6241869e68?pvs=21)
Threads #: 1
Last edited time: July 4, 2024 2:56 PM

## Preface

I had originally drafted this pre-proposal a while ago in the context that I had *fully* expected the council salary 2x proposal ( [https://pioneerapp.xyz/#/proposals/preview/890](https://pioneerapp.xyz/#/proposals/preview/890) ) to get rejected or expire (it must be voted on within 2 days or it will expire).

It certainly seems like it was one of the most contentious recent proposals, but it turns out that it somehow wasn't rejected and actually got approved by 2 successive councils. The only other proposal that I can recall as being so contentious was the same proposal type, with the same amount requested and at the time it generated an extreme amount of discussion and mostly negative sentiment in the comments as well as a lot more on Discord: [https://pioneerapp.xyz/#/proposals/preview/439](https://pioneerapp.xyz/#/proposals/preview/439)

While the DAO seems to have general agreement on things like roadmaps, OKRs, runtime upgrades, plans/reports and budgets (that one is debatable) it seems that after all of the changes that have happened and things that mostly get agreed upon on a day to day basis, the absolute extreme deal breaker for everyone is daring to change how much the council gets paid—it is the highest role on the DAO so maybe that has something to do with it.

Joystream was built with a very high-friction mechanism to prevent a council from just paying itself a ton of money and perhaps for that reason or many others, all other attempts have failed and to date no one has been able to present a viable way of rewarding the council based upon specific work or performance. This is an extremely hard problem to solve because performance means building an entire scaffold (like the FM program was) exclusively to measure council performance.

Anyway, *somehow* for the first time in 1 year, 6 months and 1 day—the council salary was finally actually adjusted from the “default setting”, and it was not for a lack of trying because there have been at least a few attempts at changing it, all with very different ideas and rationales and numbers behind them…

| **Date** | **Title** | **Link** | **Proposed Reward (per block)** | **Rationale** | **Outcome** | **Was it discussed and re-proposed with a slightly different number/rationale?** |
| --- | --- | --- | --- | --- | --- | --- |
| December 9th, 2022 | Mainnet launch | [https://joystream.subscan.io/block/1](https://joystream.subscan.io/block/1) | 0.385 | Genesis Block / Default Value | Genesis Block / Default Value | Genesis Block / Default Value |
| March 3rd, 2023 | 2x The Council Salary | [https://pioneerapp.xyz/#/proposals/preview/439](https://pioneerapp.xyz/#/proposals/preview/439) | 0.77 | “Council Member is one of the most demanding roles, the reward should be increased" - I actually submitted the proposal because we still weren’t listed on an exchange and I wanted to start pushing the idea of moving on from the FM program. | Rejected. Amount was too high, other salaries were too low. A bonus performance scheme was mentioned. | Nope. |
| September 10th, 2023 | Adjust Councilor Rewards | [https://pioneerapp.xyz/#/proposals/preview/525](https://pioneerapp.xyz/#/proposals/preview/525) | 0.32 | I think the idea was to cap it to 20% of the total budget so that it would fit within 750k budget increment. | Rejected/abstained because the proposal wasn’t developed enough | Nope. |
| March 12th, 2024 | Shift From Fixed Council Rewards | [https://pioneerapp.xyz/#/proposals/preview/835](https://pioneerapp.xyz/#/proposals/preview/835) | 0 | Council work isn’t evenly contributed to by elected CMs, put salary at 0 and have rewards be paid out via spending proposals. | Cancelled by runtime upgrade execution 27 hours after it was submitted. | Nope. |
| May 22nd, 2024 | 2x Council Reward | [https://pioneerapp.xyz/#/proposals/preview/890](https://pioneerapp.xyz/#/proposals/preview/890) | 0.77 | Council reward hasn’t been changed since mainnet launch. Every other role has had their salary reviewed. Council reward is too low—mentions that ideally we should pay based upon performance/outcomes but no one has identified a way to do this. | Passed | It passed but I am guessing if it hadn’t the answer here would’ve been nope. |

I do actually find some relief in seeing that the council pay has finally adjusted and I provided a very lengthy rationale for my approve votes: [https://pioneerapp.xyz/#/proposals/preview/890?showVote=OLYMPIA-7833392-2](https://pioneerapp.xyz/#/proposals/preview/890?showVote=OLYMPIA-7833392-2) It being the most contentious proposal type and with such a short voting period really does not leave a new council with much time to think things through.

I do not see having a high council salary as a permanent solution to some of the problems I will identify in this pre-proposal and am aiming to solve--it is very much a band-aid to deal with a longstanding problem that hasn’t had an easy solution and I think the council should be adjusting the council salary more regularly. I even tried to highlight a viable way in which it could be used basically every council term: [https://pioneerapp.xyz/#/forum/thread/906?post=6596](https://pioneerapp.xyz/#/forum/thread/906?post=6596) but it didn’t seem to get any interest.except for one by l1dev) so it is perhaps a little unsurprising that they all failed.

# The Problem

I wrote quite an extensive review of Joystream governance in this thread: [https://pioneerapp.xyz/#/forum/thread/927](https://pioneerapp.xyz/#/forum/thread/927) Part of the suggestions I made were to incorporate separating some council tasks to specific people and people have long suggested linking the council salary to specific outcomes.

This and some other initiatives are a bit hard to pull off for various reasons, however it appears that there is now a feasible way to launch a "General Purpose DAO/Joystream Multisig" in a way that makes it a lot easier to use than before: [https://pioneerapp.xyz/#/forum/thread/928](https://pioneerapp.xyz/#/forum/thread/928) 

This means that a body that is fairly independent of the council can pay for certain governance/council tasks as an independent body along with a vesting schedule that makes these tasks an attractive role within the DAO. Some of them could maybe be achieved via working groups, but maybe some can't--it is very hard to say. Certainly rewarding councils for performance based outcomes would end up with the council likely paying itself.

I think at this point one of the problems I have identified with governance is that consistency is sometimes difficult to achieve and also unpredictable due to election outcomes and people are maybe not willing or able to commit to a full council term (especially since the terms are now 28 days long).

There are some parts of DAO operations and processing that do not really fall under the council's direct purview as the work is done quarterly or at a cadence that does not directly flow with council elections. It seems currently that the skillsets required for owning and fulfilling these parts doesn't really get any consideration for remuneration and is probably somewhat underappreciated by voters--people do not see the hours of meetings and work and research that go into some things. Regardless, they are extremely important for the DAO to have.

Prior to this proposal passing an elected council member was set to receive about $55 USD in $JOY per day which simply put does not really act as enough of, or even close to a realistic incentive for people with the kind of skillsets that the DAO requires in governance work that involves long term planning, discussion, attending many meetings, execution, alignment and periodic reviews. Unfortunately, due to blockchain limitations it is not possible to have the council salary paid with a vesting schedule--unless the council were to do it itself, which can cause many unforeseen issues and consequences.

It is often said that the council(s) are the ultimate decision makers and arbiters of the DAO and while this is somewhat true, in reality the council is technically only actually responsible at a blockchain level of just voting on proposals--there is no mandate that they actually do any specific amount of work, work any specific hours or do work to any set standard of quality. I very much hope to address that problem with this pre-proposal.

This problem also sometimes means that people may be asked, expected or just decide in good faith to contribute by their own goodwill for free which is unfair, inefficient and can lead to long term issues such as knowledge gaps, poor flow of information, lack of accountability and most critically: unpredictable results.

In the worst outcomes, such critical work:

- Get totally unappreciated
- May be delayed unreasonably (due to the person being unpaid)
- May not get completed at all or forgotten about because no one is actually assigned to do it in the first place. Just because it has been practice up until now that certain elected people do certain tasks this should not be counted on forever.
- Get completed to a lesser or different standard by someone else, who "takes over" the work because they were elected
- Not receive necessary followup (especially in the case of pre-proposals and some tasks)
- In the case of this type of work being handed over to someone else informally, purely based upon election outcomes, would likely mean there will be inefficiencies and delays in communication that slow things down tremendously.
- In the case of work being done by contractors/3rd parties, a lack of continuous ownership has already resulted in tremendous delays and inefficiencies because the next council had a different composition than the last.

This is especially noticeable when there are going to be specific policy decisions that seem to be of more interest to voters than the skillset of election candidates - I think that this is a natural evolution of elections and I am certain that this will continue over time and it is probable that the specific policy stances that council candidates make may do more to influence election outcomes than the applicant's ability to do specific high-level, long term work.

The type of work I am going to define below is critical for the DAO to be able to deliver consistently and reliably as it forms the bedrock of the shared goals and vision for what the DAO is doing - it is a bigger communication, coordination and consensus tool than anything else we have. Without these things it makes it extremely difficult to plan and deliver based upon long term goals.

## Solution

During the testnet period it was actually envisioned that there would one day be a `Council Tasks Rate Sheet` that would include some of the things that I am going to describe: [https://github.com/Joystream/community-repo/blob/master/archives/council/council_tasks_rate_sheet.md](https://github.com/Joystream/community-repo/blob/master/archives/council/council_tasks_rate_sheet.md) -- this idea if followed today would mean there is at least some separation of certain tasks from council's that are elected and also mean that there are incentives for people to work on critical tasks that may take longer than 1 or even several council terms to be planned, designed, discussed, implemented and reviewed.

The first thing that needs to be done is to establish a "General Purpose DAO/Joystream Multisig" so that the council does not end up in situations where it is judging its own work and paying itself: [https://pioneerapp.xyz/#/forum/thread/928](https://pioneerapp.xyz/#/forum/thread/928) This needs to be composed of trusted, long term community members who ideally have staked roles and can exercise reasonable judgement and are active participants who know the project inside out.

## The Work

I suggest that at minimum these tasks should be broken away from the typical elected council system and be directly assigned to people(s) who possess the necessary skillset and knowledge of our DAO structure to be able to complete them with not only predictable and more consistent and timely outcomes but also to be incentivized directly for doing so.

### 1. OKRs

OKRs are set in quarterly intervals and the DAO has recently taken steps towards making these more effective and nuanced than previous iterations. They are now built as cascading OKRs. OKRs are critical in that they help to better align the DAO, the council and various working groups in terms of direction, priorities and resource allocation and help to set goals/commitments with attached outcomes that are measurable--these are typically done quarterly and have taken several iterations to start to reach the improved state that they currently have.
OKRs are also central to being able to measure performance of certain working groups and the DAO in general in achieving goals that it sets - this means that the OKRs not only act to give the DAO a sense of agency with specific targets, but also critically mean that the DAO is capable of self-efficacy ([https://en.wikipedia.org/wiki/Self-efficacy](https://en.wikipedia.org/wiki/Self-efficacy))

> self-efficacy is an individual's belief in their capacity to act in the ways necessary to reach specific goals
> 

Needless to say, I think the quote above illustrates perfectly how important OKRs are. They obviously require a *dedicated* person or persons to gather them, take feedback from WGs and other parties, organize meetings, ensure documentation is done adequately and that they either conform or aspire to eventually conform to best practices in this area. While there is obviously some fantastic feedback and suggestions for topics like the OKRs that get into specific details--it is the person responsible for working with OKRs duty not to come up with all of this feedback themselves, but to be able to productively utilize the most viable suggestions to improve and better align the OKRs.

I do not know how many hours this "task/role" takes as I have never done it myself and don't have the necessary skillset to do it--should it be paid based upon milestones? should it be a flat rate? I don't know, that needs some discussion.

### 2. The Roadmap

The roadmap of the project is a critical task that has never really be owned by any single person besides myself (tomato). It is linked to directly on the project's homepage and forms as one of the most critical areas that users, researchers and potential investors of the project will look at to be able to form some understanding and appreciation of the medium/long term plans that the DAO (and also JSG) are working on. Again--demonstrating self-efficacy is extremely important here, and the roadmap does this just as much as the OKRs.

The roadmap naturally requires someone who has an in-depth understanding of the project, the ability to organize information well, communicate well, an understanding of the DAO's structure as well as the ability to field suggestions from community members who may present good ideas but may at times also present ideas that are infeasible for many reasons.

The roadmap is typically only updated once per quarter, and probably takes 40+ hours to fully organize and deliver each iteration.

### 3. Budgets / Economics / Tokenomics

A constant problem that we have is that budgets aren't dealt with by a dedicated person--although we do have some tooling, the information conveyed in our plans and reports is quite limited.
To date, the DAO has generated:

- 8 vested discretionary payments from WG events
- 321 WG budget refill events
- 1,665 council budget refill events
- 4,281 discretionary payment events
- 30,000+ WG payment events (probably, I don’t actually know the number because my sync tool breaks)
- This doesn't include any NFT sales/auctions, CRT market activity and a number of other things.

Although the council has a tool to generate reports, it is more like a summary of budgets rather than a detailed look into the above events. What is needed is a person who is dedicated to parsing budget events via custom tools and able to categorize payment events with labels and an organization system--especially as the DAO begins to utilize more complex financial decisions like vesting schedules and we begin seeing increased CRT activity.

I tried to build such a tool using a spreadsheet but it often has issues and crashes a lot, so is inappropriate for this purpose.

I think we need a budget person along with a good idea of what we expect out of that person. I do not know if we have anyone on the DAO who could do this just yet

### 4. DAO Secretary

The Council Secretary was a longstanding role that existed within Joystream's testnets and the task of this role was basically to organize information, take ownership of pre-proposals and other governance related issues and to try and ensure that the council is mindful of any outstanding issues or potential conflicts that may arise due to older proposals or agreements.

As mainnet has evolved the title of this role no longer appears to really be that relevant, as it suggests that this secretary should be beholden to the currently elected council directly and only deal with issues that the council has--it seems more like the person fulfilling this role should be beholden to the DAO as a whole and with that responsibility be able to exercise some degree of autonomy and report on issues that may be extremely inconvenient and decisive at times.

The DAO Secretary is required to organize information that the DAO produces via labels and linking within a database that would look something a little like this: [https://joystream.notion.site/d0b1c51337c3405aa5a471bbbaa11d63?v=e504db66d15c4da6bc9fe45228b0bfb9&pvs=4](../Council%20Tasks%20d0b1c51337c3405aa5a471bbbaa11d63.md) (where relevant proposals and forum threads are linked to issues, prioritized, categorized, tracked and followed up on)

They must basically be omnipresent ("the all seeing eye") and look at all tangents of the DAO at all almost all times, regardless of council or WG composition. They must generally attend almost all meetings, keep track of almost all developments across the DAO both on-chain and off-chain (such as GitHub) even if they aren't directly related to governance and in general it is a full time job that works asynchronously.

They must also do some other things like:

- be able to identify where there are gaps in the flow of information and suggest improvements
- be able to identify issues with governance
- make sure governance parameters etc are properly discussed and reviewed for periodic runtime upgrades
- suggest periodic reviews of governance policies and parameters in a way that is as neutral as possible
- draft periodic pre-proposals and proposals to gather information, collect this information and create proposals that try to reach a consensus on things
- ensure that templates and versioned proposals are used as often as possible
- review plans/reports, budget proposals and all other types of proposals and pre-proposals and suggest improvements or issues with information presented

This is obviously a full time role.

### 5. Other things

There are probably some other things that could also be separated from the council role. I will leave that open to discussion.

### 6. (eventually) paying the council based upon performance

I do not think we should do this as a first step but rather have it as a gradual goal.

# Feedback

I would love to hear people’s thoughts on this topic.