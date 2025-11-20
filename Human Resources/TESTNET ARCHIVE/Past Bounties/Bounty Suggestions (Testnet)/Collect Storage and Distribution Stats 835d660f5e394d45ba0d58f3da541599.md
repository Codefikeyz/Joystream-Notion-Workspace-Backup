# Collect Storage and Distribution Stats

Status: Ready to use
Specification: Distributors, Storage
Submited by: l1dev

@HR please help to turn this into a regular governance bounty with a weekly reward of 3M (gardually widening the scope to produce output similar to previous council minutes):

Title: Collect Storage and Distribution stats
Cover: [https://cdn.discordapp.com/attachments/933726271832227911/960082414653288489/unknown.png](https://cdn.discordapp.com/attachments/933726271832227911/960082414653288489/unknown.png)
Description:

Develop a script to collect all information asked about Storage and Distribtion WG required for the council report.
[https://www.notion.so/joystream/Council-Report-1-f4b9f93df5d9444cb2326eae1f2eeb3c](https://www.notion.so/f4b9f93df5d9444cb2326eae1f2eeb3c?pvs=21)

Or if that is faster collect all information manually and document sources/queries used:
- Storage [https://discord.com/channels/811216481340751934/812344681786507274/960082549156225045](https://discord.com/channels/811216481340751934/812344681786507274/960082549156225045)
- Distribution [https://discord.com/channels/811216481340751934/933726271832227911/960082137770516500](https://discord.com/channels/811216481340751934/933726271832227911/960082137770516500)

Weekly delivery is needed  by the council every term within 24h after finalization of the last block. Automation is preferred.

![Untitled](Collect%20Storage%20and%20Distribution%20Stats/Untitled.png)

Found this in my notes, has a bit more possibly helpful detail:
DISTRIBUTION REPORT

Create a dashboard visualizing following data based on data served by
-

[https://query.joystream.org/graphql](https://query.joystream.org/graphql)

-

[http://orion.joystream.org/sp-dashboard](http://orion.joystream.org/sp-dashboard)

-

[https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)

- contact JSG for updated dumps

[https://discord.com/channels/811216481340751934/822087161104957470/953223452922368012](https://discord.com/channels/811216481340751934/822087161104957470/953223452922368012)

# Report
The working group report should include a special section with information about
- What data objects were permanently lost.
- How many bags were created.
- How many bags were deleted.
- How many data objects were downloaded, and
- what was their total size,
- what was the size distribution.
- Distribution of bag sizes in terms of data object counts.
- Distribution of bag sizes in terms of total data object size.
- Total capacity of all distribution bucket limits.
- Total used capacity of all distribution buckets.

Hint:

[https://git.joystreamstats.live/Operations/jsstats/src/frontend/src/components/Distribution](https://git.joystreamstats.live/Operations/jsstats/src/frontend/src/components/Distribution)

fetches some of the data and has relevant queries.