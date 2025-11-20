# leaderboard queries

[https://joystreamstats.live/](https://joystreamstats.live/)

[https://dev.joystreamstats.live/](https://dev.joystreamstats.live/)

1. Council Terms
    1. [Elected Councils](https://www.notion.so/Elected-Councils-7a8045d228ad410f840f9bf6081f34b5?pvs=21) 
    2. 
    
    | id | electedAtBlock | endedAtBlock | isResigned | councilMembers/0/member/handle | councilMembers/1/member/handle | councilMembers/2/member/handle |
    | --- | --- | --- | --- | --- | --- | --- |
    | 00000001 | 0 | 345601 | true |  |  |  |
    | 00000002 | 345601 | 561602 | true | isonar | abramaria_ | ismail |
    | 00000003 | 561602 |  | false | 0x2bc | l1dev | jen4ph |
    - `electedAtBlock` until `endedAtBlock`
    - `isResigned` = false means council term is still active
2. Memberships
    1. `chainstate` : **`members.nextMemberId` at blockhash of council end block**
3. Channels
    1. `chainstate` : **`content.nextChannelId` at blockhash of council end block**
4. Videos
    1. `chainstate` : **`content.nextVideoId` at blockhash of council end block**
5. NFTs
    1. Cannot be done via chainstate
    2. [All sold NFTs + Price + Video name + buyer name](https://www.notion.so/All-sold-NFTs-Price-Video-name-buyer-name-3b9e80a96a014787b00cae8c397c6cf7?pvs=21) will list out all NFT sales (not NFT issuance!)
6. Forums
    1. Categories `chainstate` : **`forum.nextCategoryId` at blockhash of council end block**
    2. Threads `chainstate` : `forum.nextThreadId` **at blockhash of council end block**
    3. Posts `chainstate` : `forum.nextPostId` **at blockhash of council end block**
7. Validation
    1. not my area of knowledge
8. WGs
    1. Number of workers: `chainstate` : **`forumWorkingGroup.activeWorkerCount` at blockhash of council end block**
    2. WG budget refills: [WG Budget Refill Events](https://www.notion.so/WG-Budget-Refill-Events-5a24af7bbded4cdca260ffe6de2c969b?pvs=21) 
    3. Worker Payments: [Workers Payments + WG name + isLead](https://www.notion.so/Workers-Payments-WG-name-isLead-d7278566771b43fc982c35bd8b8589d0?pvs=21) 
    4. WG Discretionary Spending: [WG Discretionary Spending](https://www.notion.so/WG-Discretionary-Spending-aef320616da34a04ac46f908a46dd11a?pvs=21) 
9. Minting
    1. CM payments: [Council Payment events](https://www.notion.so/Council-Payment-events-f739a71de4c8444dafb8038789a79261?pvs=21) 
    2. Council Budget Refills: [Council Budget Refill Events](https://www.notion.so/Council-Budget-Refill-Events-02d51f5b504147d3b42c2026155ccc10?pvs=21) 
10. Proposals
    1. [All Proposals for leaderboard](https://www.notion.so/All-Proposals-for-leaderboard-5b839c9b9278423eb4f92bacff841b33?pvs=21)