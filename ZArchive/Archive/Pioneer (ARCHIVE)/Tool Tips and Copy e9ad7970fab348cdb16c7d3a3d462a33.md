# Tool Tips and Copy

# My Profile

![My_profile.png](Tool%20Tips%20and%20Copy/My_profile.png)

| Tooltips | Copy | Comment |
| --- | --- | --- |
| Total Balance | Total balance from all connected accounts. This includes transferable and locked balance. |  |
| Total Transferable Balance | Total Balance less locked balance. Transferable balance can be used for signing transactions on the network. |  |
| Total Locked Balance | Staking, or bonding, is the act of locking up funds under some terms so that they are not transferable and otherwise not entirely usable as they otherwise would be. The terms, referred to as *unstaking terms*
 describe the circumstances under which the funds may begin to cease being staked. 

The way staking is implemented is with the use of account [locks](notion://www.notion.so/joystream-handbook/key-concepts/staking) | 
Link to > [https://joystream.gitbook.io/joystream-handbook/key-concepts/staking#locks](https://joystream.gitbook.io/joystream-handbook/key-concepts/staking#locks) |
| Total Recoverable Balance | Stakes are recoverable, unless slashed. Slashing is the act of reducing the balance of an account by some amount, and also reducing the size of the lock which represents the use case under which the slashing occurs. | ⚠️ **Validate**: Stakes are recoverable, unless slashed.

**You may have staked something which is not recoverable at any given time, but eventually it will be unless you get slashed.**

❓Any other reasons? 
**NO**

Also, is there an option to recover balance and pay the fee from the transfer?
**I did not understand this question.**
 |

![Edit Membership.png](Tool%20Tips%20and%20Copy/Edit_Membership.png)

| Tooltips | Copy | Comment |
| --- | --- | --- |
| Root Account | Root account is used to create membership and sign membership updates. All other transactions on the network are signed with controller account. | **Validate>** ⚠️All other transactions on the network are signed with controller account.

**YES** |
| Controller Account | Controller account is used to sign transactions. |  |

| Component | Copy | Comment |
| --- | --- | --- |
| Paste a URL of your avatar image. | Paste a URL of your avatar image. | Remove “Text lorem ipsum” |

![Screenshot 2022-02-07 at 16.28.03.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_16.28.03.png)

| Tooltip | Copy | Comment |  |
| --- | --- | --- | --- |
| Transaction Fee | Transaction fee covers the cost of processing the update and storing the record on the chain.  | ❓ How is it calculated for all transactions?
**TLDR: each transaction has a weight function, constructed by the developers through a process called benchmarking. This function takes possible parameter inputs to the transaction and returns a notion of “weight”, which you should think of as the worst case computing time on some reference hardware spec, for processing the transaction. The main driver of this weight is how many times the transaction wil need or right to the underlying state database of the node. This weight is converted into a fee, in terms of $JOY, using a weight-to-fee function, however this function is currently just f(x) = 0 for Olympia, so all transactions will have 0 in $tJOY processing fees for all trans. Separately from this there is also a fee which simply comes from the amount of block space it takes to embed the transaction in the block it gets included in. So obviously, if you have large parameters (like text for video descriptions) this costs more. There is an analogous way to charge $JOY in terms of bytes of space occupied. I belive this also will be 0 in all cases for Olympia, but htis actually should be checked :P, which I will do.**

ℹ️ Handbook is empty on fees> [https://joystream.gitbook.io/joystream-handbook/key-concepts/fees](https://joystream.gitbook.io/joystream-handbook/key-concepts/fees) |  |

![Screenshot 2022-02-07 at 16.28.38.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_16.28.38.png)

| Component | Copy | Comment |
| --- | --- | --- |
| Invite Member - Insufficient Working Group Budget  | Memberships Working Group budget has to be sufficient to cover new member invitations.

Speak with the Membership Working Group Lead > on Discord to find out about the upcoming funding proposals for this group. 

Link > | Working Group Lead > points to #/working-groups/membership

Learn more points to > [https://joystream.gitbook.io/joystream-handbook/subsystems/membership#working-group](https://joystream.gitbook.io/joystream-handbook/subsystems/membership#working-group)
 |
| Working Group Dept | Working Group Debt | Typo Dept → Debt |
|  |  |  |

![Screenshot 2022-02-07 at 17.03.01.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.03.01.png)

| Component | Copy | Comment |
| --- | --- | --- |
| Creation Fee Tooltip | Creation fee is the price of membership, it is managed by council through the proposal system. 

Transaction fee for membership creation is paid separately. 

Link > | Link > [https://joystream.gitbook.io/joystream-handbook/governance/proposals](https://joystream.gitbook.io/joystream-handbook/governance/proposals)
 |

# Working Groups

## Openings

![Screenshot 2022-02-07 at 17.05.51.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.05.51.png)

| Tooltip | Copy | Comment |
| --- | --- | --- |
| N/A |  | no tooltips identified |

## Working Group

### Openings

![Screenshot 2022-02-07 at 17.29.44.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.29.44.png)

| Tooltip | Copy | Comment |
| --- | --- | --- |
| Current Budget | The budget is the root resource pool for all token minting in the working group, and the size of the pool is denoted by budget.

Link >
. | Link to > [https://joystream.gitbook.io/joystream-handbook/governance/working-groups#budget](https://joystream.gitbook.io/joystream-handbook/governance/working-groups#budget) |
| Working Group Debt | If funds are insufficient over payout periods, the working group can incur a debt, which is owed to workers.  | + Rename to “Working Group Debt”

❓ Can we rename to “Owed To Workers” 
**Probaby better yes**

How is it defined in the system? Is there a limit to it?
 |
| Avg Stake | Worker roles require staking in order to apply and remain in the role. Staking for worker roles is done using a designated working group lock on a single account per worker role.

Link > | Link > [https://joystream.gitbook.io/joystream-handbook/governance/working-groups#staking](https://joystream.gitbook.io/joystream-handbook/governance/working-groups#staking) |

### About

![Screenshot 2022-02-07 at 17.32.53.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.32.53.png)

| Tooltip | Copy | Comment |
| --- | --- | --- |
| Total Spending | Total spending of the working group in  | ❓ Is this counter linked to council election period or starts since the beginning of times?

**I think so yes.** |

### My Roles > Role Activities

⚠️ Screenshots are from Figma

![Screenshot 2022-02-07 at 17.36.17.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.36.17.png)

![Screenshot 2022-02-07 at 17.35.28.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.35.28.png)

![Screenshot 2022-02-07 at 17.36.25.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.36.25.png)

# 

| Tooltip | Copy | Comment |
| --- | --- | --- |
| Hiring complete | Hiring complete!

We are sorry, your application was not successful this time. We encourage you to explore alternative openings and subscribe to notifications. | 

 |
| Role Ended | Your role is now terminated.  | ❓ is this rationale or just generic text?

**I am not actually sure what cases “Role Ended” is meant cover? Is it only if they are terminated? what if they choose to leave? there is a rationale in both cases, but in the latter it would be provided by the worker initiating the exit, in which case it would not make sense for them to see their own rationale.

I actually think that, even if it is only restricted to the former, the rationale provided by the lead is likely to be a much more extensive report than what fits in that little box, so you may want to just keep a generic placeholder there, and perhaps offer them the ability to read the full rationale? do they have this option to read the rationale for why they were terminated somehwere else? if not, that probably should be something to add at some point after Olympia.** |
| No applicants yet | Be the first one to apply. |  |

# Proposals

![Screenshot 2022-02-07 at 17.53.50.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_17.53.50.png)

| Tooltip | Copy | Comment |
| --- | --- | --- |
| Proposal Stage = Deciding | Initial stage for all successfully created proposals. This is the only stage where votes submitted can actually impact the outcome. If a new council is elected, any present stake is slashed by rejection fee, the staking lock is removed and the proposal transitions to the rejected stage. |  |
| Proposal Stage = Dormant | Proposal was approved by current council, but requires further approvals to satisfy constitutionality requirement, which is a minimum number of consecutive council votes. Transitions to deciding stage when next council is elected. |  |
| Proposal Stage = Gracing | Is awaiting execution for until trigger block. If no trigger was provided, then awaiting for gracing limit blocks, since start of period. When this duration is over, the execution conditions are checked, if they are satisfied the proposal transitions to the execution succeeded stage, if they are not, it transitions to the execution failed stage. |  |
| Proposal Stage = Vetoed | Was halted by SUDO, nothing further can happen. This will be removed at mainnet. |  |
| Proposal Stage = Rejected | Was rejected with full stake penalty by the current council. |  |
| Execution Succeeded | Execution succeeded, nothing further can happen. |  |
| Execution Failed | Execution failed due to unsatisfied execution conditions, nothing further can happen. |  |
| Rejected | Proposal was rejected by council. Rationale can be checked in proposal details, and nothing further can happen. |  |

### Creating New Proposal

### ___

Add New Proposal

![Screenshot 2022-02-07 at 19.09.50.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_19.09.50.png)

| Tooltip | Copy | Comment |
| --- | --- | --- |
| Empty State - Proposals | The proposal system is the way changes to the platform state and policy are suggested, discussed, voted on by the council, and finalized as accepted or rejected. |  |

![Screenshot 2022-02-07 at 18.15.26.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.15.26.png)

| Copy | Copy | Comment |
| --- | --- | --- |
| Top  | A proposal is a motion to change the state or policy of the system in some way. While we encourage you to make proposals that benefit the network, there are certain risks associated with proposals. |  |
| Highlighted text box | - proposals can get rejected by the council
- a rejection fee will be withheld upon stake recovery from rejected proposals
- you may get outright slashed, losing your entire stake. This applies only to some proposal types | ❓ is rejection fee something that is paid ON TOP of regular stake recovery signing transaction fee
**YES, think of it like a bond which is included to discourage swamping the council in malicious, frivolous or poorly reasoned/explained propositions.**

⚠️ What are slash-able proposal types, how are they presented?
**This is a parameter associated with each proposal, so Pioneer will need to just read this from the system. We can only change this with a runtime upgrade, but Pioneer ideally should be written in a way where it can dynamically grab this from the chain.** |
| CTA  | Create A Proposal > | ❓ DM: I think this wording of “I want to create a proposal anyway” is worded almost to discourage from creating proposals - is that intentional?

**No not really, change if you please.** |

![Screenshot 2022-02-07 at 18.15.05.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.15.05.png)

### Proposal Types

![Screenshot 2022-02-07 at 18.06.47.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.06.47.png)

| Proposal Type | Explainer | Comment |
| --- | --- | --- |
| Signal | Think of signal as the *what*, whereas rationale parameter in other proposals would be the *why*. Signal proposal does not effect any platform parameters when accepted. 

** | ❓ how often is it used in the platform and why?

**Likely very often, I think it is the most important proposal on our testnets so far. It is meant to coordinate around some sort of commitment which likely non-technical in nature, so having to do with policy or process or something like that.** |
| Set Initial Invitation Balance | Invitation balance is deposited to new member’s account to cover basic transactions. This balance can only be used on fees. |  |
| Set initial invitation Count | New members have default allocation of new members invite. Invites can be transferred to other members. |  |
| Set Membership Lead Invitation Quota | Membership Workgroup Lead is automatically assigned invitations upon taking the role. This proposals is aimed on managing this invitations count. |  |
| Set Referral Cut | Referrals, same as new membership invitations are incentivised by the platform. Referral cut entails the reward to the originator of invitation links which resulted in new memberships. |  |
| Create Blog Post | Council blog | ❓ 
Why do we need blog posts again? 

**We probably wont. There is no UI for this in Pioneer, I dont even know if there are any proposals for it really in the runtime (there might), but 76% sure its going away.**

Forum threads are not covering this objective? |
| Edit Blog Post | Unlocked blog post can be edited. |  |
| Lock Blog Post | When a post is locked it can no longer be modified. |  |
| Unlock Blog Post | Unlocked post can be modified. |  |
| Veto | Veto for a particular, previously issued proposal. Vetoed proposal is automatically discarded. | ❓ 
Is the stake getting automatically slashed in the pointed proposal? 

**I don’t know actually, I did not think we had this proposal even? Where are you getting this? I think this is an idea, but don’t think anyone implemented this.

Update:** https://github.com/Joystream/joystream/issues/1982 |

![Screenshot 2022-02-07 at 18.06.39.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.06.39.png)

| Proposal Type | Explainer | Comment |
| --- | --- | --- |
| Slash Working Group Lead | Same effect as slashing worker in the group, the staking account gets slashed. |  |
| Set Working Group Lead Reward | Same effect as updating the reward of the worker.  |  |
| Terminate Working Group Lead | Same as when terminating a worker in group with given inputs, and removing lead designation. |  |
| Amend Constitution | Proposal to amend constitution. Does not effect platform parameters. | ⚠️ **Validate:** Does not effect platform parameters. 

**Correct** |
| Cancel Working Group Lead Opening | Same as when cancelling an opening for workers in the given group with given inputs. |  |
| Set Membership Price | Sets new membership price. |  |
| Set Council Budget Increment | This proposal sets how much tokens is added to council budget every new budget period. This budget is spent on working groups, spending proposals and council rewards. | ⚠️ Validate

**Correct** |
| Set Councillor Reward | All councillors are paid out the same flat reward rate from the councillor budget, subject to budget constraints.  | ⚠️ Validate

**Correct** |

| Proposal Type | Explainer | Comment |
| --- | --- | --- |
| Runtime Upgrade | Proposal to upgrade version to the new runtime. |  |
| Funding Request | Request to credit council budget and transfer tokens to specified accounts.  |  |
| Set Max Validator Count | Specifies maximum allowed validator workers on the platform. |  |
| Create Working Group Lead Opening | Same effect as when creating an opening for workers in the given group with given inputs, except the opening type is for lead. |  |
| Fill Working Group Lead Opening | Same effect as when filling opening in group for worker with given inputs. |  |
| Update Working Group Budget | If budget update is non-negative, then this amount is reduced from the council budget and credited to the group budget, otherwise the reverse. |  |
| Decrease Working Group Lead Stake | Same effect as when decreasing worker stake in group with given inputs. |  |

![Screenshot 2022-02-07 at 18.06.31.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.06.31.png)

### Proposal General Parameters

![Screenshot 2022-02-07 at 18.07.31.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.07.31.png)

| Tooltip | Copy |  |
| --- | --- | --- |
| Sliding Drawer - How to write good rationale? | The purpose of rationale is for council and community to understand the implications on the platform, reasons behind the proposals and actions to be taken. 

Keep it short and snappy. Write in short sentences and stick to 2-3 sentences per section. 

1. Concrete Desired Outcome

Start with the desired outcomes of this proposal. What are you trying to achieve? How exactly and in what way will this impact the platform and the community? 

2. Reason

Good to set the background, specify the reason for this proposal. What problem does it solve? Why did this become a problem?  

3. Action Plan

Explain how you suggest to solve the problem and achieved desired outcomes. What resources, timing and community effort is required to solve it?

4. Alternative Solutions

Have you considered any alternative solutions? How to solve this problem if this proposal is rejected?

5. What can go wrong

List possible issues and risks to achieve the desired outcomes, if this proposal is accepted.  |  ❓ How to write a good rationale?

⚠️ Keep it short and snappy. Write in short sentences and stick to 2-3 sentences per section. 

**Looks good**

❓—> what sort of behaviors do we want to drive here?

**People are writing proposals which other people understand, in a word: clarity.
Also perhaps what we want is for people to understand that the idea must be clear in their own mind, so if they have not fleshed out exactly what they are wanting to do and why, they need to go back and do additional work.

Another thing which is also perhaps importnat to let people know is that they may want to start conversations about a proposal in advance of submitting them, asking for feedback, etc. so that they already have it calibrated in terms of any domain specific parameter values (e.g. how much money they are asking for).

It could make sense for us to make a video tutorial or something about this, but for now this text form information has to do.**
 |
| Tooltip - Trigger | Set up the proposal to get triggered in the future, on a specific block count. |  |
| Tooltip - Discussion Mode | Proposal thread is created as part of the process. Here you may chose to enable discussion among the selected list of members. |  |

![Screenshot 2022-02-07 at 18.07.45.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.07.45.png)

![Screenshot 2022-02-07 at 18.08.02.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.08.02.png)

# Council

![Screenshot 2022-02-07 at 18.46.08.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.46.08.png)

| Tooltip | Copy |  |
| --- | --- | --- |
| Total Rewards Missed | Total rewards missed. Missed rewards happen due to ..  | ⚠️ ❓ what is missed reward?

**Rewards that were attempted paid, but could not due to budget having run out. This is not the same as debt, because debt is your current negative balance, which could get returned to 0, missed reward can only go one way: up.** |
| Total Spent on Proposals | Total council budget spent on proposals, including funding proposals. More details on proposals spending can be found in the Overview module >. | Overview hyperlinked to > [https://pioneer-2.vercel.app/#/overview](https://pioneer-2.vercel.app/#/overview) |
| Total Paid Rewards | Council Rewards paid to council members. | ⚠️ is this to council members

**Yes** |
| Total Spent | Total budget spent in this council on working groups, spending proposals and council rewards. |  |
|  |  |  |

# Election

![Screenshot 2022-02-07 at 18.41.44.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.41.44.png)

![Screenshot 2022-02-07 at 18.41.14.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.41.14.png)

![Screenshot 2022-02-07 at 18.40.53.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.40.53.png)

![Screenshot 2022-02-07 at 19.09.28.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_19.09.28.png)

| Tooltip | Copy |  |  |
| --- | --- | --- | --- |
| Staking microcopy | You must stake {{xyzk Joys}} to announce candidacy. This stake will be return to you if your candidacy fails as a result of the council voting.  |  |  |
| Election Round | Elections are held in consecutive rounds. This is the number of current election. |  |  |
| Revealed Votes | Votes are kept anonymous and get revealed during the reveal period, after voting is complete. Only revealed votes are counted. |  |  |
| Stage | Elections occur periodically, and each one has a sequence of stages referred to as the election cycle. Stages are: announcing period, voting period and revealing period. 

More details>  | LInk points to > [https://joystream.gitbook.io/joystream-handbook/governance/council#election](https://joystream.gitbook.io/joystream-handbook/governance/council#election) |  |
| Period Remaining Length | Remaining length of current period before the next one starts. 

Link > | Change Title to 

”Period Ends in”

Link from tooltip points to > [https://joystream.gitbook.io/joystream-handbook/governance/council#election](https://joystream.gitbook.io/joystream-handbook/governance/council#election) |  |
| Election Round | Current election round. 

Elections occur periodically, and each one has a sequence of stages referred to as the election cycle. Stages are: announcing period, voting period and revealing period. 

Link > |  |  |
| There are no Candidates yet | Be the first one to announce your candidacy.  |  |  |
|  |  |  |  |

# Forum

![Screenshot 2022-02-07 at 18.54.00.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-07_at_18.54.00.png)

⚠️ Change validation to active button, and “This field cannot be empty. Type your message here.”

# Members

N/A

# Settings

N/A

# Bounties

![Screenshot 2022-02-10 at 20.32.37.png](Tool%20Tips%20and%20Copy/Screenshot_2022-02-10_at_20.32.37.png)

[Tooltips and Copy ](Tool%20Tips%20and%20Copy/Tooltips%20and%20Copy%2077112750649c41b39626b050cddd0c14.md)