# EVM/smart contracts viability

Public Notion URL: https://joystream.notion.site/2d6f0adb12204966848439bfe1dbff53
Priority: Medium
Tags: builders WG, runtime
Created time: June 8, 2024 3:36 AM
Work Status: Not started
Governance Status: Pre-proposed
Archive Status: No
Days passed since task created: 529
Threads: EVM/smart contracts viability (https://www.notion.so/EVM-smart-contracts-viability-277a822923b34d79a5db17dfca7253be?pvs=21)
Threads #: 1
Last edited time: June 14, 2024 8:30 PM

## Problem

Joystream doesn’t have smart contract/EVM support. This means that development of certain new features is very slow and tedious and that creative uses of our blockchain are severely limited and require expensive, slow and risky runtime upgrades. The lack of smart contract/EVM support also limits the appeal of our project to developers and ideators and experimenters because the amount of knowledge required to work with substrate is extremely high and unique

Before Joystream launched, many, many ideas were thrown around that could have been really interesting—but they were not a priority or part of the MVP. This was a little disappointing but now that we are on mainnet, I would love to start experimenting with things. What is holding me back is that ideas can’t really even be approached right now. I have created a table to illustrate why.

| **Method** | **Speed of development** | **Risk** | **Limitations** | **Further explanation** |
| --- | --- | --- | --- | --- |
| Build/improve runtime pallets | Extremely slow | Extremely high | Expensive to develop and there are some limitations to consider with scaling. Limited number of people know how to deal with substrate/polkadot-SDK | Should only really be used for stable features. Given the slow development pace and the number of substrate developers available this is not very appealing. |
| Metaprotocols | Moderately slow (it seems like adding stuff to the query node takes quite some time and can introduce problems) | Low (low in terms of risk to the blockchain) / Medium if counterparties have to be used for payments/stake | Cannot deal with stake, payments etc directly. / Cannot trigger extrinsics/payments / Must rely on counterparties to deal with payments which is extremely slow and also carries some risk | Things like this entire forum could be replaced by one some day in the future (if it becomes desirable). This would allow for new forum features to be added much more quickly.  |
| web2 services and just deal with payments using a counterparty (such as a lead/staked role) | Very fast | Very low for development / Medium if counterparties have to be used for payments/stake | unknown | This would be stuff like Zealy or comparable dashboards etc |
| Smart contracts | Relatively quick and also don’t have to go through governance | Unknown, or at least not fully explored / Malicious people could make bad/fraudulent smart contracts / Smart contracts probably need to be audited/vetted / It is unknown how smart contracts could impact the blockchain speed/performance/capacity (there are people on our project who are a lot more qualified to answer this than I am) |  | Smart contract offer a way for external developers to participate without having to build metaprotocols, runtime upgrades or even fully know how to work with Substrate/our blockchain. /They can work without having to go through the builders WG and can create incentive schemes and other highly attractive ideas without having to go through governance and council budget considerations. |

I am not a programmer, but I can imagine there is a world of opportunities available with smart contracts beyond anything I know of. In any case, I have had many, many, many ideas that I want to implement into Joystream, and these may be very attractive ideas that can completely distinguish 
Joystream from any other project. such as: 

- Votebox - video competitions/subcommunities: [https://github.com/Joystream/community-repo/issues/926](https://github.com/Joystream/community-repo/issues/926)
- Sprocket - a concept I spent more than a year on for building video communities with an advertising component and a highly, highly novel way to reward creators: [https://github.com/Joystream/joystream/issues/1966](https://github.com/Joystream/joystream/issues/1966)
- “Hashtags as payment channels”: [https://github.com/Joystream/joystream/issues/2163](https://github.com/Joystream/joystream/issues/2163)
- Idea: Paid Playlists: [https://github.com/Joystream/joystream/issues/2055](https://github.com/Joystream/joystream/issues/2055)
- Idea: Live Logo: [https://github.com/Joystream/joystream/issues/1987](https://github.com/Joystream/joystream/issues/1987)
- Idea - Curated Invitation List: [https://github.com/Joystream/community-repo/issues/148](https://github.com/Joystream/community-repo/issues/148)
- Community Calendar: [https://github.com/Joystream/pioneer/issues/51](https://github.com/Joystream/pioneer/issues/51)

There are also some other ideas by people that indicate the other possibilities with smart contracts:

- Idea: Smart contact controlled members
    - [https://github.com/Joystream/joystream/issues/3907](https://github.com/Joystream/joystream/issues/3907)
- How can EVM DAOs trigger uploads in storage system
    - [https://github.com/Joystream/joystream/issues/2040](https://github.com/Joystream/joystream/issues/2040)

# Solution

- Investigate and discuss the viability of adding an EVM pallet to Joystream
- Try to ascertain the resource cost of adding this vs possible benefits
- Implement an EVM pallet

---

---

1. Implementing an EVM pallet
    - with some limited amount of integration between the EVM + native pallets, lets assume
        - content pallet (NFTs, videos)
        - projecttoken
        - some way to accept/return/slash stake as well as do payments and have some concept of an oracle role—something kind of like the bounty module
2. Building a new pallet that can:
    - deal with the projecttoken and content pallet
        - be able to buy/own CRTs, NFTs and channels etc
    - some way to be able to mange stake (i.e. hold/return/slash)
    - some way to deal with payments (i.e. the smart contract would have to be able to “own” an address or something like that)
    - deal with concepts like a marketplace for advertising (i.e. bidding, auctions, time triggers)
    - also deal with concepts like communities + voting for particular content (basically a token curated registry)
    - and also do the above with some amount of flexibility which allows for iterative changes
3. Complete/adapt the current bounty module with some added features to try and do what is mentioned above.

My use case is to build something like this: [https://github.com/Joystream/community-repo/issues/926](https://github.com/Joystream/community-repo/issues/926) as well as build things like an advertising system—in truth there are probably a few concepts that might be possible to combine into the bounty module somehow as they are somewhat similar, but it seems like the most inflexible option and there would be some tradeoff and it seems like future changes would be hard.