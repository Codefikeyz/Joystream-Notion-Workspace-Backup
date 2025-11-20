# Agenda wc 13th Dec

Participants: Netguru Design, Klaudiusz
Created By: Dima
Type: Weekly Tech-Design Sync
Created: December 13, 2021 7:54 PM
Last Edited Time: December 21, 2021 12:28 PM

# Agenda

- [ ]  Review [to-dos from last week](https://github.com/Joystream/atlas/issues/1539):
    - **🚨 [@TCzechowski](https://github.com/TCzechowski) to initialize the discussion regarding "Time Blocks" in the NFT MVP epic GitHub issue.**
    - **🚨 [@toiletgranny](https://github.com/toiletgranny) to document decisions and create design guidelines for large numbers & date formatting,**
- [x]  Design Epics Roadmap view:
    - [x]  Discuss start/ end dates for in progress epics in relation dev team expected pace of delivery
        
        Link to roadmap view>
        
        [GitHub - Joystream/atlas: UI for consuming Joystream - a user governed video platform](https://github.com/Joystream/atlas#workspaces/atlas-600edbb8799cc700103bc2d7/roadmap)
        
    - [x]  When does each team member gets free from currently planned work ?
- [x]  NFT non-mvp scope brought up:
    - [x]  Which user stories discussed on Monday, was it quick wins or next set of "should-haves"?
    - [ ]  Do we have any stories that are designed/ or can piggy-back from current MVPs in terms of components etc
    

# Notes & Todos

1. There's a bank holiday in Poland that's not reflected in the team's abscence table.
    - [x]  @Netguru Design (Adam) to update the abscences table for the design team
2. In regards to timed auctions for NFTs, we decided to keep displaying the full countdown in the app (eg. on the Video NFT page, or on the transaction finalization view), along with the blocks countdown as a secondary piece of information. Once the time countdown goes below 60 seconds, the timer is replaced with "less than a minute" text (ideally, of a prominent styling). Alongside, there should be an info icon displayed whenever there's an auction time countdown, hovering upon/tapping on which should bring up a tooltip with a brief explanation on how the countdown works in Atlas.
    - [x]  @Dima to provide a copy for the tooltip mentioned below,
        - [ ]  "When the timer gets below 1 minute, use blocks count down for last minute-bidding.
            
            Joystream is implemented on a blockchain, and in such a system, the way it evolves is by having blocks of operations, called transactions being committed, one after the other, to a public ledger. Time duration on blockchain is calculated in blocks, and not clock time. Each block takes around 6 seconds on average to get produced. Combining this way of calculating time with the effect of network latency makes it impossible for the app to show correct countdown timer in clock seconds with precision when it is nearing the end of countdown."
            
    - [x]  @Netguru Design (Tomasz) to update his designs accordinlgly (transaction finalization view)
    - [x]  @Netguru Design (Nina) to take the above under consideration when resuming work on the the Video page design,
    - [x]  @Netguru Design (Kuba) to reconsider the experience of issuing an NFT and setting up a timed auction, in the context of whether it makes sense to translate the user's datetime selection into a # of blocks, as an additional help information in the UI.
3. [x ] For datetime inputs we decided to go with browser's native datetime pickers for now, instead of creating a custom component.
4. We've discussed and updated start & end dates if selected NFT epics in the Design Epics Roadmap view.
    - [x]  @Netguru Design (Adam & Nina) to review end dates for their "Projects" and let Dmitry know once it's done.
5. We've talked about non-mvp NFT scope based on user stories provided initially by Bedeho.
    - [x]  @Netguru Design to review & update the [spreadsheet with the list of user stories](https://docs.google.com/spreadsheets/d/1AcS4mLXo8ybMwmBx93jwhpqtnEhn4nIVKokTOHtiAe4/edit#gid=0) and mark the ones that could potentially be quick wins in terms of the next steps.