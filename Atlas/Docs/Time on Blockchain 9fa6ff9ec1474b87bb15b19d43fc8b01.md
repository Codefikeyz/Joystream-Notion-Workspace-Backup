# Time on Blockchain

Created By: Dima
Created: December 6, 2021 4:14 PM
Last Edited Time: December 15, 2021 12:21 PM
Last Edited By: Netguru Design

**What exactly is a time block?**

I am not sure I have used this exact term, but let me try to explain. Joystream is implemented on a blockchain, and in such a system, the way it evolves is by having blocks of operations, called transactions typically, being committed, one after the other, to a public ledger. These operations are things like "issue NFT" or "publish video", and so on. Now on our system, the clock time between blocks is stochastic, not deterministic, but on average, it is supposed to take 6 seconds. So for 10 blocks to pass, it would take, on average, 60 seconds. Now all notions of time in the blockchain, as we use it, are in terms of block numbers, not clock time. So when when the user selects some duration in Atlas, like say "I want to have bidding for up to 50 days", what is happening under the hood in the app - before anything goes to the blockchain, is that 50 days is converted into 50 days * 24 hours/day * 60 min/hour * 60 seconds/min = 4320000 seconds, which then is converted to a total number of blocks by doing 4320000 seconds/6 = 720000 blocks. This value is actually sent to the blockchain, and the business logic in the blockchain only computes and stores these kinds of notions of time. Conversely, when Atlas is to display clock time to a user, based on what is stored in the chain at a given time, it has to do the reverse calculation.

**Also, we will display that “Ending in:” timer on English auctions, but are we able to show the EXACT time there?**

When referring to events in the future, then no, because the time between blocks is stochastic, so you can really only display expected time, but the error should not be that substantial, however it probably increases with duration of the interval. In pioneer this sort of thing has been solved by displaying both clock time and actual blocks, so people focus on whatever is most important to them, but most people dont have a problem with the small degree of unpredictability in milestone times.

![C3C3B07C-BCFA-4801-8561-62A602FCDF2E.png](Time%20on%20Blockchain/C3C3B07C-BCFA-4801-8561-62A602FCDF2E.png)