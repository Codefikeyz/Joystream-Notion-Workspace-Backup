# n8n integration brief for Builders WG

Public Notion URL: https://joystream.notion.site/95ee5e24af9346d89fcf29c3058dad22
Tags: Integrations, builders WG, council, forum, governance, proposals, tooling
Created time: April 3, 2024 5:19 PM
Owner: tomato
Work Status: Done
Governance Status: N/A
Archive Status: No
Days passed since task created: 595
Last edited time: April 8, 2024 6:24 PM

## Update as of 8th April, 2024

- Builders WG support no longer required

## Background

There is currently no organizational system for governance and proposals, this makes it difficult to organize things and to make governance work with regularity. Notion is a powerful tool and getting both proposals and forum threads *into* a Notion database for the following purposes:

- Building a proper governance/council workflow for dealing with pre-proposals, proposals and other things
- Organization: assigning labels, assigning “owners”, assigning due dates, assigning WGs
- Maintaining a list of `active` and `inactive` governance proposals
- Maintaining a list of `unresolved` pre-proposals
- Using parent/child relationships between Notion databases to organize information for quick retrieval and to also correlate it to council terms
- Using parent/child relationships to assign WG/council plans and reports to council terms

Without going into details this specific problem has had multiple attempts at being solved—there have probably been several thousand hours spent on trying to solve this problem and there is a quite easy solution to this that I will outline below. I do not have programming skills so am unable to complete it myself.

## Solution

- [n8n.io](http://n8n.io) is a low-code workflow automation tool, similar to Zapier or IFTTT
    - It supports GraphQL queries as well as Notion.
    - This means it can be set up to read GraphQL queries for proposals and forum threads and import them into a Notion database.
    - It can either be paid for or self-hosted as it is open source. I already pay for it, so it is already ready to go.
- 2 databases would be created within Notion with the necessary columns.
    - Database 1: `Proposals` (an example of this is shown below in screenshot format)
    - Database 2: `Forum Threads`

![Untitled](n8n%20integration%20brief%20for%20Builders%20WG/Untitled.png)

- [n8n.io](http://n8n.io) would then be set up to run GraphQL queries periodically and populate the 2 databases
    - 2 queries/workflows are necessary for this, one for `proposal` and one for `forum threads`
    - The “first run” of the workflow would need to import all existing `proposals` and then after that is complete, the workflow would need to only import either new `proposals` or *update* preexsting proposals on Notion with changes (such as if the `status` of a proposal changes from `Voting` to `Executed`)

A partially working workflow for `proposals` is shown in the screenshot below and attached as a .json file that can be imported into n8n.io. I can provide my credentials for n8n.

[Proposals_2_Notion.json](n8n%20integration%20brief%20for%20Builders%20WG/Proposals_2_Notion.json)

![Untitled](n8n%20integration%20brief%20for%20Builders%20WG/Untitled%201.png)

- The `Code` block above contains the following code:

![Untitled](n8n%20integration%20brief%20for%20Builders%20WG/Untitled%202.png)

- The `Compare datasets` block contains the following
    - Some data manipulation would be necessary for things like `createdAt` to make them work for a `date/time field` within Notion
    - Some data manipulation would be necessary for things like `status:__typename` to go into Notion as a `select` type field

![Untitled](n8n%20integration%20brief%20for%20Builders%20WG/Untitled%203.png)

- The `Notion (Beta)` block contains the following:

![Untitled](n8n%20integration%20brief%20for%20Builders%20WG/Untitled%204.png)

**NOTE:** about 90% of the above integration now works as intended, all that is required is some logic to update proposals that change status (i.e. if a proposal changes from being in voting stage > executed stage)

Alternative is to use Zapier but sounds more painful to setup/maintain: [https://community.zapier.com/show-tell-5/guide-how-to-use-the-monday-graphql-api-in-zaps-with-the-webhooks-app-14324](https://community.zapier.com/show-tell-5/guide-how-to-use-the-monday-graphql-api-in-zaps-with-the-webhooks-app-14324)