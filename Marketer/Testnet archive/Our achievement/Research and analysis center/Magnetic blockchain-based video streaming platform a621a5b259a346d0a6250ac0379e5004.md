# Magnetic blockchain-based video streaming platforms

![Blockchain-Enabled-Video-Streaming.png](Magnetic%20blockchain-based%20video%20streaming%20platform/Blockchain-Enabled-Video-Streaming.png)

Video streaming is decentralized, where one organization cannot control the content delivery of the streaming service. It is important to note the difference between decentralized and distributed video streaming.

Whereas distributed video streaming means that the content delivery network is spread across the world and one organization is behind it, decentralization removes that control entirely. It creates a network where participants can reach consensus on what the network will do, adding an extra layer of democracy and giving more power to the community.

Decentralized video streaming platforms are usually owned by the community. Blockchains allow ownership of the platform and are the foundation for decentralization, providing an ideal baseline for applications. The blockchain layer acts as a thin layer that connects all the pieces through a single decentralized ledger.

All off-network transactions must provide validation to the blockchain layer to verify whether the transaction is legitimate. Therefore, the blockchain becomes the only source of truth. However, because blockchains cannot store complex data sources such as video or images, off-network solutions such as IPFS or simple peer-to-peer storage make data accessible.

Peer-to-peer technology as a prerequisite for blockchain-based video streaming

While blockchain is becoming the base layer, a peer-to-peer protocol such as IPFS or BitTorrent is a prerequisite for full decentralization. Blockchains are inherently decentralized, and anyone will be able to have a copy of the entire blockchain if they decide to run their own node. On the other hand, file systems, which are usually centralized, are becoming increasingly difficult to use without a peer-to-peer protocol.

Services such as Google Cloud Storage, Amazon S3 and Azure Storage serve as examples of how efficient centralized storage can be. But to give users a fully decentralized experience, you can't rely on these technologies as part of a decentralized ecosystem.

## Technical challenges in decentralized video streaming

Monetization remains a major challenge for decentralized video streaming platforms. Compared to the convenience of centralized platforms such as YouTube, decentralized video streaming doesn't stand a chance.

In this section, however, we'll look at the technical challenges rather than purely business model issues. The first problems that come to mind include file storage and rights management. In addition, a decentralized ecosystem is not free from the need to protect the copyrights of material created by original artists. Creators should consider implementing checks and balances to discourage malicious users from trying to disrupt the ecosystem.

In a peer-to-peer network, users need to store video files and provide a reliable Internet connection for peer-to-peer connections. Finally, there is the issue of content monetization schemes. Let's take a closer look at them, analyzing possible solutions.

## The file storage problem

Peer-to-peer file systems will always face the problem of file availability. Storage is expensive, and without clear incentives, users will not put files on their systems, let alone maintain a stable Internet connection for other users to access.

As an alternative to the file sharing ecosystem, peer-to-peer file sharing can fail due to a lack of providers. You can only get your files when another peer node is online and ready to provide you with the file. Consequently, you will need at least one other peer node to share your files. In such a peer-to-peer ecosystem, creators could resort to a central relay node to provide missing files when all peer nodes are offline.

However, this would lead to the original problem of centralization. If there is a centralized force that can provide the entire community, what are the incentives for community self-sufficiency? In this case, many projects provide a solution for continuous decentralized data sharing. Projects such as Arweave , Filecoin and BitTorrent , offer different solutions to the same problem.

## Arweave

Arweave is a persistent decentralized data storage system that is mainly used for archiving on the Internet. Arweave uses a single payment scheme to ensure archive availability. Users pay upfront to archive their files online.

## Filecoin

Filecoin is a protocol that allows users to rent out available hard drive space. Filecoin serves as a peer-to-peer file system based on IPFS to allow users who have excess hard drive space to rent out their system for Filecoin mining. Filecoin may sound like a pay-as-you-go system similar to Google Drive. In my opinion, it is one of the best alternatives to peer-to-peer file systems.

## IPFS

You can also use the IPFS interplanetary file system for storage. But plain vanilla IPFS still requires you to host your files or pay for a service to host your files if you want them online. DTube , a decentralized video streaming app that is a direct competitor to YouTube, uses IPFS to store files and uses Steemit blockchain to incentivize its creators to create quality content.

## BitTorrent

BitTorrent , in my opinion, is the most interesting of the five options. BitTorrent is a peer-to-peer protocol that does not depend on users to host nodes. Instead, it uses a concept called siders and leeches. Siders are users who have uploaded files and make them available to other users, essentially using their network bandwidth to upload files to the network. Leechers are users who request a file and upload files to the file system. A swarm is the aggregate of Syds and Lickers in the BitTorrent ecosystem.

In BitTorrent, uploaders are rewarded with BitTorrent coins for their contribution to the network. In contrast, uploaders will have to spend BitTorrent tokens to download files or increase download speeds.

While BitTorrent may seem like the most decentralized option compared to the others, it relies on a central tracking server that records the IP addresses of the sitters and passes them on to requesting file listers. Like any other peer-to-peer file sharing protocol, you can't upload files if there are no sitters.

## Theta

Theta is a blockchain infrastructure that provides decentralized video streaming and is the leading and most well-known infrastructure project among those mentioned. Theta uses a centralized peer-to-peer storage called Theta EdgeStore . As part of its storage solution, Theta's decentralized storage is compatible with centralized cloud infrastructure, including AWS S3 and Google Cloud Storage. The centralized cloud provides highly reliable storage, while the decentralized part provides fault tolerance if the cost of using centralized systems is too high.

Theta will also have a peer-to-peer exchange network to help deliver streams. However, the peer-to-peer exchange network does not store video, but only helps deliver content.

## Creating an untrusted ecosystem

With a peer-to-peer video streaming ecosystem, you trust the other computers on your network to provide you with correct, unchanging data. But how do you ensure this in a peer-to-peer ecosystem? Projects like BitTorrent, IPFS and Arweave are relatively secure software. However, you should be careful enough to double-check what you download from these platforms, because the danger is mostly the files themselves.

To avoid careless storage providers and malicious protocols, Filecoin cuts its rewards to encourage good behavior. The bottom line is that providers have a skin in the game, so they have incentives to save files.

Since you will be streaming video, you will only accept the file type with the video extension. While file reliability will still be an issue, you can easily dismiss it as a potential vulnerability risk if you get a different file extension.

Also, most decentralized video streaming platforms don't allow you to directly access files. Instead, you interact with them through their web application. This gives you an extra layer of security, knowing that you won't run the videos on your device and your browser copies the videos without saving them.

Blockchain-based video streaming platforms transcode video for each device. Thus, each platform needs a secure way to transcode files for consumers. Transcoding itself can be a problem in decentralized ecosystems because there is no guarantee that each transcoder is reliable. However, by encouraging good behavior, many transcoders with skins on the line will comply or risk reduced rewards. Or, in the case of Livepeer, they risk cutting their bid.

The transcoding mechanism with proof of Livepeer's stake is similar to proof of work, requiring you to put enough Livepeer tokens as collateral. If the tokens are blocked, each transcoder has tokens they will lose if they don't behave properly, making it very expensive to attack the entire ecosystem.

Creating an untrustworthy ecosystem requires incentives for the most important players to behave properly. If there are no penalties for bad behavior, the entire ecosystem will become untrustworthy due to malware and bad user behavior.

## Streaming monetization scheme

Creating content is not cheap, and creators must earn revenue for putting their content on the platform. Revenue streams vary by platform; some use a subscription model, while others use pay-per-view or ad-based models. While not all business models are created equal, some revenue streams are better than others depending on conditions.

For example, if you want the platform to be free to use, YouTube's ad-based model may be a better approach. Chainflix might be a good example.

## Chainflix

Chainflix is a decentralized video streaming infrastructure that can act as a one-stop package for ad-based streaming. Content for streaming video is not cheap and takes a lot of effort to produce. Chainflix focuses on creating incentives for users to create good content, and provides viewers with a free content platform. Its business model is similar to YouTube because they rely entirely on advertising to generate revenue for creators.

The difference is that Chainflix uses a decentralized architecture to relinquish control over the content published on its platform and uses proof-of-view (PoV) blockchain to monetize its ads. The advantage of the PoV mechanism is that it protects the system from gamification by bots who seek to profit by watching videos. Although PoV sounds like a revolutionary concept, competition with other projects is growing. As of this writing, Verasity is leading the way.

To control the flow of content, Chainflix uses controllers to connect the client side to decentralized server storage using APIs. Chainflix also uses artificial intelligence to improve storage efficiency and create a more intelligent decentralized storage scheme. Chainflix's ecosystem focuses on efficiency rather than true decentralization, using blockchain to monetize and store content, unlike LBRY, which uses a pay-per-view model.

## Common video streaming infrastructure on blockchain

Of all the video streaming projects on blockchain, the infrastructure remains largely the same. Each video streaming infrastructure on blockchain typically consists of a smart contract, a file repository, a content transcoder, and finally an API layer.

While the common infrastructure typically uses these four components, projects like Theta also have an additional blockchain execution environment to properly scale their underlying infrastructure. But how does all of this interact with each other?

Typically, a user who wants to stream video will first access the content through the platform's application interface and API layer. Then, when the user finds the content he's looking for, he buys access to it via a smart contract and pays via cryptocurrency.

The platform can then use one of two approaches for authentication: either an expiring NFT, or they can provide content immediately without additional authentication.

Users then retrieve content through an API layer, connecting to a content transcoder and accessing the raw data inside the file repository. The content transcoder acts as a content gateway, decrypting content as needed.

While all of this sounds simple and may make a lot of sense to many people, creating a decentralized transcoder connected to decentralized storage is still a huge challenge for most. How can content creators be sure transcoders are honest? Decentralized content transcoders are not run by corporations interested in protecting video. They can be run by normal people like you and me.

Livepeer is trying to solve this problem by creating a PoS-based transcoding ecosystem in which anyone with a transcoding server would have to supply enough tokens to gain access to the network. If a malicious transcoder disrupts the ecosystem, their rate will be cut and the staking reward will cease to exist.

The next problem is the API layer. While it is one of the simplest components of a project, the API layer still needs to be centralized. Reliability is a factor to consider in most projects, and if the API layer is decentralized, you'll run into the problem of where to store all the data.

Sure, you can say you can request a smart contract. But what if the smart contract is on a platform like Ethereum with high gas fees?

You might think about creating a new blockchain execution environment. While this is possible, you end up adding an extra layer behind your API layer, complicating the project itself. NoSQL or relational database queries run faster than blockchain queries, and you can even create complex queries in databases, whereas it's effectively difficult or nearly impossible to do so in blockchain.

Even after all this fiddling, we never touched the issue of decentralized file storage. You need high reliability for video streaming, but how can you be sure that your decentralized file system is up to the task? What if it often fails on you?

You'll need to add an extra layer to the videos you show. You can use a CDN or even external storage. But storing videos on external storage outside of a decentralized file system kind of defeats the purpose. Even Theta uses cloud providers as the main building block for its video streaming ecosystem.

Sure, peer-to-peer storage is a viable alternative, but peer-to-peer storage can never surpass the consistently reliable cloud storage available to developers in today's world. This is an interesting quandary.

Conceptually, truly decentralized video streaming platforms may be one of the most challenging technical advances. Without the reliability of some cloud services, such as cloud storage, centralized APIs and databases, it's hard to create a viable streaming platform that can compete with giants like YouTube and Netflix.

## Conclusion

Blockchain is revolutionizing the video streaming industry with advanced technologies and solutions. In this article, we looked at several decentralized video streaming infrastructure projects, including Theta, Livepeer, LBRY, and Chainflix. In addition, we examined other related blockchain storage projects such as IPFS, Arweave, Filecoin and the social blockchain project Steem, which drives content creation.

Finally, we looked at how conventional blockchain-based video streaming infrastructure conceptually works and the challenges of creating a truly decentralized streaming platform.

Cryptocurrency opens up a wide range of new incentive models to maintain order in the chaos of decentralization. The most interesting thing about the blockchain video streaming space is the number of projects experimenting with different models and trying to find the most profitable and sustainable model. But only time will tell which projects will survive to the end.

*This article is based on a study by Augustinus Theodorus*