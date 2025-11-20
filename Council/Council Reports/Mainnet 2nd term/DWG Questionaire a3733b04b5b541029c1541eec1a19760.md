# DWG Questionaire

[https://discord.com/channels/811216481340751934/933726271832227911/1060801293448388608](https://discord.com/channels/811216481340751934/933726271832227911/1060801293448388608)

[Answers](https://discord.com/channels/811216481340751934/1060801293448388608/1062387995086434404)

Note: DN in questions ususally refers to Distribution Provider (DP).

# How long would it take to prepare architectural diagrams showing major conceptual, as well as logical and infrastructure parts of a Distribution Node (DN)?
This depends expected complexity and granularity.

# Is DN a cache? What will happen if user requests a piece of content that's not present on a DN?
See [https://github.com/Joystream/joystream/blob/master/distributor-node/docs/node/index.md#caching](https://github.com/Joystream/joystream/blob/master/distributor-node/docs/node/index.md#caching)

# How's the process of content distribution between storage and  DN organized? A sequence diagram in PUML format would be nice.

[https://github.com/Joystream/joystream/blob/master/distributor-node/docs/api/public/index.md](https://github.com/Joystream/joystream/blob/master/distributor-node/docs/api/public/index.md)

# Can a malicious user manipulate the DN statistics by continously requesting content via some script?
Possibly.

# Is DN storage elastic? auto-scalable? 
No.

# If a DN goes down or becomes unhealthy, will Atlas (Gleev) detect it and stop routing user requests to such a node?
No, it will pick another node though.

# Can Dapp developers control which regions to distribute their content to? Think a Dapp that only targets US East Coast audience.
Lead has control over which DP a channel is served by.

# Does the content on a DN have a TTL? Or it sits there forever?
See caching above.

# What locations are current DNs are deployed to?

[https://github.com/Joystream/community-repo/pull/869](https://github.com/Joystream/community-repo/pull/869)

# What cloud providers do current DNs use? 
dito

# Don't you find it silly that a Web3 decentralized video platform uses Web2 centralized cloud providers like AWS to run its storage and distribution infra? 
Why that tone?

# How do you plan to count video views?
ES

# How do you plan to detect bad user experience and proactively work to improve it?
Proactive tests via scripts:

[https://github.com/Joystream/community-repo/issues/744](https://github.com/Joystream/community-repo/issues/744)

[https://github.com/Joystream/community-repo/issues/745](https://github.com/Joystream/community-repo/issues/745)

# Can the DWG Lead single-handedly disconnect DNs from the network?
No it usually requires both hands.

# Can the DWG Lead single-handedly ban, blacklist, or remove content from DNs?
No

# Can DN operators ban, blacklist, or remove content from DNs they operate?
They can drop files of course. Monitoring has to pick up on it to take according penalty. This can be automated.

# Are DN operators supposed to pay Storage operators for content they copy over from Storage nodes?
No.

# Do Joystream distribution have any kind of [SLA]([https://aws.amazon.com/cloudfront/sla/)?](https://aws.amazon.com/cloudfront/sla/)?)
No, legal representation is expected to lie withing the DAO.