# General purpose DAO/Joystream multisig

Public Notion URL: https://joystream.notion.site/c529d6123bcb4b708ff6500283f809ec
Priority: Medium
Tags: compensation, council, governance, multisig (joystream), subDAO
Created time: June 9, 2024 9:27 PM
Work Status: Needs follow up
Governance Status: Pre-proposed
Archive Status: No
Days passed since task created: 528
Threads: General purpose DAO/Joystream multisig (https://www.notion.so/General-purpose-DAO-Joystream-multisig-cd9fc0de773446289c6adf330ecd4e55?pvs=21)
Threads #: 1
Last edited time: June 20, 2024 11:40 AM

NOTE: with the Argo runtime upgrade happening soon, there is a pre-proposal which stipulates that we need to elect a “JoyOp” multisig to control parts of the bridge on Joystream’s side—that is a totally different thing to what I am describing here and that is also of a much higher priority: [https://pioneerapp.xyz/#/forum/thread/920](https://pioneerapp.xyz/#/forum/thread/920)

## Problem

- It has long been suggested that the council should be paid based on performance and delivery, here are some examples of discussions like I have linked below. The difficulty in doing this is that it would end up with the council directly paying themselves and can lead to situations where there is an extreme conflict of interest
    - [https://pioneerapp.xyz/#/proposals/preview/890?post=1072](https://pioneerapp.xyz/#/proposals/preview/890?post=1072)
    - [https://pioneerapp.xyz/#/forum/thread/874](https://pioneerapp.xyz/#/forum/thread/874)
- It has also long been suggested that the DAO may benefit from having a $JOY multisig that is controlled by some long term community members who are active participants.
    - This could be for emergency uses
    - This could also just be a fund outside of the council treasury that has utility for several things
- The previous tooling for multisigs was very early and didn’t work well.
    - It was thought that Joystream multisigs would have to change their addresses if any member of them changed, but with the introduction of the proxy pallet it is now possible to avoid this: [https://pioneerapp.xyz/#/forum/thread/897?post=6480](https://pioneerapp.xyz/#/forum/thread/897?post=6480)
    - I believe there are now things like NovaSpektr (a desktop wallet from the Nova team) that incorporate multisigs a lot better
- I guess the DAO could use this multisig to put some tokens into staking as an added security, but this area is very unclear and uncerain

## Solution

- Draft a charter/proposal of what the multisig will do and how it should be composed
- Figure out how much funding should be added to it
- Form a Joystream multisig that is elected by the council