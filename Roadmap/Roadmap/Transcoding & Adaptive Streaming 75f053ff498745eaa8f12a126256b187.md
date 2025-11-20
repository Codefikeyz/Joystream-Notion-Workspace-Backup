# Transcoding & Adaptive Streaming

Description: Users access content across a wide range of browser, devices, applications and also under heterogeneous and dynamic bandwidth constraints. As it stands, only a single version of each media asset is represented in our metadata standards and backend node software. This means have now way to represent a broad range of encodings and resolutions for media assets, let alone produce all of these. Introducing server-side transcoding in Orion will unlock this, and many other future benefits that come from server-side post-processing (thumbnail extractions, auto-subtitling, etc.). It will also unlock the ability to do adaptive streaming, where a user with a dynamic connection can more quickly see asset resolve and play, and also be able to watch videos under suboptimal circumstances.
Team: JSG
Products: Atlas, Orion, YPP
Council Approval Status: Not started
Work Status: In progress
ETA: October 1, 2023 → December 31, 2023
ETA (Quarter): 2024 Q4
Roadmap v2 Feasibility Notes: per klaudiusz, dao can probably get involved with this
Roadmap v3 Feasibility: - per klaudiusz, based on discussion with JSG, it is possible this will be delivered in Q2 (at least some version of it)

- already being worked by zeeshan + JSG

- per bedeho is plausible. depends on how elaborate solution is, but v1 is viable. will change the way uploads are done, they will upload to orion instead, would change YT sync etc
Y/N: yes
Roadmap v4 Feasibility: - per bedeho, its a POC, so still needs testing/refining etc + changing of UI/UX, backlogged due to other priorities