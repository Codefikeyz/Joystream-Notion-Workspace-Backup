# Lenstube.xyz

![68747470733a2f2f6173736574732e6c656e73747562652e78797a2f696d616765732f6272616e642f62616e6e65722e706e67.png](Lenstube%20xyz/68747470733a2f2f6173736574732e6c656e73747562652e78797a2f696d616765732f6272616e642f62616e6e65722e706e67.png)

## Lenstube - is a decentralised social media video sharing platform created using the Lens protocol

![2022-08-23_19-27-07.png](Lenstube%20xyz/2022-08-23_19-27-07.png)

Lens Protocol is a composable and decentralized social graph, ready for you to build on so you can focus on creating a great experience, not scaling your users.

The Lens Protocol is a Web3 social graph on the Polygon Proof-of-Stake blockchain. It is designed to empower creators to own the links between themselves and their community, forming a fully composable, user-owned social graph. The protocol is built from the ground up with modularity in mind, allowing new features and fixes to be added while ensuring immutable user-owned content and social relationships.

Lens Protocol seeks to solve major issues in existing social media networks. Namely, Web2 networks all read from their unique, centralized database. There is no portability. Your profile, friends, and content are locked to a specific network and owned by the network operator. This causes each network to fight a zero-sum game for your attention.

Lens Protocol corrects this by being a user-owned, open social graph that any application can plug into. Since users own their data, they can bring it to any application built on top of Lens Protocol. As the true owners of their content, creators no longer need to worry about losing their content, audience, and livelihood based on the whims of an individual platform's algorithms and policies. Additionally, each application using Lens Protocol benefits the whole ecosystem, turning the zero-sum game into a collaborative one. Developers can design meaningful social experiences without needing to turn to feedback mechanisms to lock in a user's attention.

The purpose of the Lens Protocol is to empower creators to own the links between themselves and their community, forming a fully composable, decentralized social graph. This is achieved by allowing users to create profiles and interact with each other via these profiles. "Profile" (as used here) refers specifically to Lens profiles; "user" refers to standard crypto-wallets.

The protocol is built from the ground up with modularity in mind. Lens Protocol is currently overseen by a multisig, which will be expanded to a broader DAO, which can develop and vote on new modules and expanded functionality.

## **Architecture**

Let's first dig into profile creation and publishing. Users must create a profile on the hub, for which they will receive a sequentially ID'd profile NFT. This NFT controls the profile, and thus, its owner becomes the de facto controller of the given profile.

Profile owners can:

1. Publish to the profile. Publication types are:
    1. Post: A standard piece of content.
    2. Comment: A standard piece of content with a pointer to another publication.
        1. Since comments include a pointer, this executes the pointed publication's "reference module" logic, if any.
    3. Mirror: The equivalent of a "share" in a traditional sense, having no content but a pointer to another publication.
        1. Since mirrors only include a pointer, this executes the pointed publication's "reference module" logic, if any.
2. Set the profile's "follow module":
    1. This whitelisted logic contract determines the logic that must be executed when a wallet attempts to follow the given profile; for example, some followers may incur a fee to the profile owner via the fee follow module contract.
3. Set the profile's image URI
4. Set the profile's "dispatcher":
    1. This is an address that can act on behalf of a profile's owner; it can:
        1. Publish to the given profile.
        2. Set the given profile's URI.

Regular wallets can:

1. Follow profiles:
    1. This executes the profile's "follow module" logic, if any.
    2. This mints the following wallet a "follow NFT" unique to that profile and sequentially ID'd.
        1. Follow NFTs have a custom URI set by profile owners.
2. Collect publications:
    1. This executes any logic in the publication's "collect module."
        1. If the publication is a mirror, this is executed on the originally mirrored publication with a referral.
    2. This mints the collecting wallet a "collect NFT" unique to that publication and sequentially ID'd.
        1. Collect NFT URIs point to the collected publication's URI.

# Built-In Governance

Follow NFTs include built-in governance mechanisms -- any profile can spin up a DAO in minutes!

![2022-08-23_19-29-50.png](Lenstube%20xyz/2022-08-23_19-29-50.png)

## **Follow NFT Overview**

When following a profile, followers obtain a FollowNFT, which is the core building block of the Lens Protocol social graph! From a technical perspective, these NFTs contain governance-specific logic that allows for the following:

- Power delegation (via delegate())
- Power delegation by meta-transaction (via delegateBySig())
- Fetching power at a specific block number (via getPowerByBlockNumber())
- Fetching total delegated supply at a specific block number (via getDelegatedSupplyByBlockNumber())

Note that by default, delegation is inactive, so followers need to delegate, either to themselves or to another trusted user to partake in governance!

Now that's cool and all... But how do you *use* this to build a *DAO?*

## **Just DAO It!**

![2022-08-23_19-30-33.png](Lenstube%20xyz/2022-08-23_19-30-33.png)

To spin up a DAO, all you've got to do is deploy a contract that interfaces with the Follow NFT's built-in functionality. It should allow for proposal creation and interface with the given profile's Follow NFTs to read governance power at the appropriate blocks for voting -- that's it!

In a nutshell, a governance contract would need to handle...

- Proposal creation
- Voting with FollowNFTs at the given past snapshot (facilitated by the aforementioned FollowNFT functions!)
- Proposal Queuing
- Proposal execution

But this is just a basic list of requirements and only scratches the surface of what's possible!

### **Tokenization**

The Lens protocol has three layers of tokenization via ERC721 NFTs. All three are ERC721-compliant and fully composable.

The LensHub upgradeable contract is the core entry point for the majority of interactions in the Lens Protocol. Nearly all interactions begin and doubles as the ERC721 NFT contract for profile NFTs, which are minted upon profile creation.

Upon a profile's first follow, a FollowNFT contract is deployed (via minimal proxy cloning), unique to the profile; this is the ERC721 NFT contract that represents follower positions.

Lastly, upon a publication's first collect, a CollectNFT contract is deployed (again, via minimal proxy cloning), unique to the publication; this is the ERC721 NFT contract that represents collected publications.

Note that follow and collect NFTs are deployed only upon the first follow/collect, respectively. This reduces gas overhead for profile creation.

### **Modularity**

Modularity is at the core of the Lens protocol. Everything is built with community expansion and the continued development of new, innovative features in mind.

Modules are standalone, governance-whitelisted contracts that adhere to a specific interface. They hold state and are unlimited in potential scope beyond adhering to the interface.

There are three types of modules:

1. Follow modules:a. These modules are tied to a profile and contain logic to be executed upon a user attempting to follow the given profile.
2. Collect modules:a. These modules are tied to specific publications (except mirrors, which cannot be collected) and contain logic to be executed upon a user attempting to collect the given publication.
3. Reference modules:a. These modules are tied to specific publications and contain logic to be executed upon a user attempting to comment or mirror the given publication.b. Note that the original content and its reference module are used in the case where a mirror attempts to point to a mirror.

## Safety

To ensure the safety of the Lens Protocol’s users and promote the development of a robust, constructive network, the protocol will be launched in a guarded manner, that is, controlled by a community multisig consisting of trusted parties throughout the Web3 ecosystem. The signers will be announced before the mainnet launch so stay tuned

This multisig will be able to authorize the following actions:

- Setting up Governance and Emergency Admin Addresses
- Setting Treasury Addresses and Fees
- Whitelisting Assets
- Moving the Lens Protocol System into a PublishingPaused or fully Paused state
- Whitelisting addresses to create profiles
- Whitelisting Follow, Collect, and Reference Modules
- Upgrading the Lens Protocol Hub Contract

Notwithstanding its abilities, the multisig will not be able to do the following:

- Coopt, affect or otherwise move funds from any user of the system
- Burn any Follower or Collect NFT
- Burn or edit any non-Lens NFT
- Take any action on any other deployment of the Lens Protocol

## **Closing Notes**

The Lens Protocol is a composable social graph protocol built to be community-owned and ever-evolving. It empowers its users by allowing them to decide *how* they want their social graph to be built and how they want it to be monetized, if at all.

Furthermore, the protocol is engineered with the concept of modularity at its core, allowing for an infinitely expanding amount of use cases. This, from the user's perspective, translates to a new paradigm of ownership and customization that isn't possible (or financially feasible) in Web2.