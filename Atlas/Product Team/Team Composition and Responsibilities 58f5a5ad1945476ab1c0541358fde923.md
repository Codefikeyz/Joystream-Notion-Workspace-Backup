# Team Composition and Responsibilities

**💠 Background**

Klaudiusz has shared that his availability for JSG from 3rd of October (today) will be reduced and expressed the intention of moving to a part-time working schedule, for circa 20 hours per week. JSG is committed to offering the flexible working schedule for the service providers, and support such cases in circumstances deemed favourable for the overall business operations. On that basis, JSG executive team has made a decision to support Klaudiusz in this transition.

Following a consultation with Klaudiusz, the new schedule, working the first half of the week (Monday, Tuesday and first half of Wednesday) will be adopted for the foreseeable future. As part of this change, there will be a significant impact on the current operations, as he has a set of key technical of operational responsibilities which are not shared by other members of the team. I will be working on handling this change and during the transition time we need to ensure that impact on the overall operations is minimised.

💠 **Goal**

1️⃣ Empower: Give greater autonomy and ownership of large pieces of Atlas product and infrastructure to remainder of the team, to increase overall productivity, quality of work and initiative.

2️⃣ De-risk: There is a risk that the rest of the engineering team and project overall is left with large technical and operational blind spots during his absences, which will inevitably impact our ability to maintain the current velocity of product development and speed of decision making.

3️⃣ Unblock: With reduced working hours, he will have less time to serve tasks which enable other team members: Atlas dev team, Design Team, Query Node and marketing website developers.

💠 **Proposal**

Here is the attempt to summarise the changes which are believed to achieve the described goals within the constraints we have.

**PR Reviews**

Everyone in the Atlas dev team will receive write access, effectively having maintainer status, and reviewers can and should autonomously merge PRs they believe are completed.

Klaudiusz will provide a reviewer guideline which outlines best practices for what a reviewer should keep in mind before merging.

Whenever a mistake occurs in production, effort will be made to back track to original review process to ensure best practices are being followed, and understand how we possibly are falling short in systematic ways.

**Maintaining Playgrounds**

Every developer on the Atlas team will receive maintainer access to the playground, so they have the ability to redeploy QN, debug infra failures, etc.

**Designs**

Everyone on the Atlas team does design reviews specifically in order to provide feedback on how upcoming designs may need to be adjusted or changed to respect certain technical constraints imposed by infrastructure they are responsible for.

When required anyone should participate in ad-hoc calls to explain technical feasibility or constraints to design team. This would be done on the basis of proximity to the context of the issue in question.

[@Dima](https://joystreamworkspace.slack.com/team/U03A9NAG325) is specifically responsible for doing copy editing.

**Query Node**

[@bartosz](https://joystreamworkspace.slack.com/team/U039ZQ75P36), with support from Klaudiusz, will transition into the role of QN technical owner for Atlas stream and have primary responsibility for:- writing schemas+mappings

- review designs from QN feasibility POV
- integration: managing Atlas side code integration.
- detect failures in production: question, do we have notifications for this? we should add this as a feature to setup if not
- debug QN failures.
- work with Hydra devs (Zeeshan, Mokhtar, Leszek) to resolve possible Hydra bugs.
- Reviews are done by both.

**Orion v1, Social Previews & Faucet**

[@Rafał P](https://joystreamworkspace.slack.com/team/U03AA2T0JG1) will have primary Orion v1, Social Previews and Faucet responsibility for- engineering: writing new features and fixing any bugs

- integration: managing Atlas side code integration.
- deployment
- detect failures in production: question, do we have notifications for this? we should add this as a feature to setup if not

Note: Orion v2 will be a new powerful backend to Atlas, but work will not commence before for a few months.

**Monitoring Github**

[@Dima](https://joystreamworkspace.slack.com/team/U03A9NAG325) will have exclusive responsibility to review and triage all new Github issues originating from team or external

**Meetings**

- QN weeklies will be deprecated to support the overarching motion of decentralising this product development, and doing the QN work in the respective teams (Atlas/ Pioneer/ Infra)
- Klaudiusz will be exempt from regular participation design synchs (monday & wed), and invited on an optional basis in cases where sycn conversation can not be substituted by async collaboration on the technical feasibility matters
- YPP calls will be deprecated, since the project is nearing completion and further dev can be coordinated in the async mode
- No more regular network release calls for Klaudiusz: Dima will convey relevant information

**Community**

All engineers+ [@Dima](https://joystreamworkspace.slack.com/team/U03A9NAG325) should be present in project Discord, and taggable under `atlas-dev` handle. They should check daily for:- tags from DAO particpants about errors or problems

- bugs posted in chat which are not getting relayed to Github properly

**YPP Infrastructure related issues**

[@Klaudiusz](https://joystreamworkspace.slack.com/team/U039QEH6ZQE) will have primary responsibility for integration, and

[@Zeeshan](https://joystreamworkspace.slack.com/team/U039YA679AP) is still software maintainer and deployment resource.

💠 **Change Management and Implementation**

Nearing the mainnet launch and in-line with the objective of flattening the operations and empowering individual contributors to the protocol and the DAO, that JSG team has been taking since inception, this transition to more shared responsibilities and interchangeability between team members is taking us a step further to this goal.Please bear in mind that this is a process that involves transition of many aspects at once, and all affected participants should feel absolutely free and at ease to suggest any potential improvements, provide feedback on piloting the change and feel empowered suggest any other areas that left uncovered.Anyone is free to either reply with questions and comments to this post for the benefit of everyone else, or alternatively you can send any questions and requests to myself via dm. We can also discuss any aspects of this announcement in more detail on our Design Weekly Sync and Dev Grooming meetings.