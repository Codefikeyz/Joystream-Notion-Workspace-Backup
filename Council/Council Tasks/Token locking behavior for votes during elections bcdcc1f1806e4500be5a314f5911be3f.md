# Token locking behavior for votes during elections

Public Notion URL: https://joystream.notion.site/bcdcc1f1806e4500be5a314f5911be3f
Priority: N/A or finished
Tags: builders WG, elections, runtime
Created time: April 3, 2024 3:04 AM
Owner: tomato
Work Status: Done
Governance Status: Discontinued
Archive Status: No
Days passed since task created: 595
Threads: Token locking behavior for votes during elections (https://www.notion.so/Token-locking-behavior-for-votes-during-elections-045b4ee77fad4b7d9ea2c85d8feaab13?pvs=21)
Threads #: 1
Last edited time: June 20, 2024 5:14 PM

### Problem

Previously, voters would vote during an election and could basically immediately release their tokens once the election was finished--this means they can sell and use the tokens however they please.

Recently, we had the `nara` runtime upgrade and one perhaps unforeseen change when the election was extended from 14>28 days was that tokens used for voting are now locked for quite some amount of time (14 days+) due to the extended idle period. This only applies to votes that are both revealed and go towards successful candidates.

When tokens are `locked` like this it means that the user cannot send them and use them for some other purposes, so if the token price changed and a user wanted to take advantage of that, they would be unable to until the `idle` period finished.

This is *not* a bug of the system and was the way the system was always designed to work: [https://handbook.joystream.org/system/council#election](https://handbook.joystream.org/system/council#election) It is just that the extended lock period wasn't really that publicized during development.

The table below shows the current behavior (and to repeat: This only applies to votes that are both revealed and go towards successful candidates **for the current election**--for votes cast in older elections they can be released at any time and for votes cast against losers, they can be unlocked as soon as the idle period starts)

| **Stage** | **Announce** | **Vote** | **Reveal** | **Idle** |
| --- | --- | --- | --- | --- |
| **Duration** | 6 days | 4 days | 4 days | 14 days |
| **Lock Status** | Tokens can be released | Votes are cast, tokens are locked | Tokens are locked | Tokens are locked |

### Solution / Feedback

- The runtime *could* be adjusted to change this, so that votes can be unlocked straight after the election finishes and once the idle period starts. This would have to be discussed with the builders WG if people want it to be changed and it would have to be prioritized and implemented based upon resources available to fix something like this. It would also require testing and being placed in a runtime upgrade
- Is this a **good** or **bad** thing? What do people think?

As usual, I will not share my own thoughts in this opening post to keep it fairly neutral and may share them in a later post.

20th June, 2024

Nothing actionable was suggested in the pre-proposal