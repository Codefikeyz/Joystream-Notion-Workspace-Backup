# Storage operations and Content Distribution Network

Agenda: Storage operations and Content Distribution Network
Tags: Storage Operations, Training, Workshops
Date: November 10, 2023
Recording: N/A
Venue: Community Voice 1 channel
Status: Done
Facilitator: @Yasir
Duration: 54mins
Moderator: Codefikeyz
Attendance: vikan
codefikeyz
0x2bc
igrex
mayortee
genius
spat_sochi
Transcript: N/A

## Meeting Note

---

**Storage Architecture**

- Yasir presented the basic architecture of how the storage works. The storage node puts data and retrieves data from the blockchain, while the query node reads stuff from the blockchain. The replication policy is used to replicate an object in multiple locations to prevent losing objects.

**Replication Policy**

- Codefikeyz asked about replication and its application in new payments where workers are paid for their used storage capacity. Yasir explained that when a channel is created, servers are chosen randomly, but there's an element of geolocation involved as well. He also mentioned that increasing replication means increased disk usage and costs.

**Chain as Reality**

- When making payments, data is drawn from the chain because it represents reality even if it's different from what's on a server due to channels being created but not yet replicated.

**Geolocation**

- There's an element of geolocation involved in assigning storage servers when creating a channel according to Yasir who said they're still documenting this parameter.

**Storage and Query Node**

- Yasir discussed the importance of the query node in relation to storage servers. He explained that all components inject messages into the chain and read from it to understand what's happening. The only way to read this chain is through a query node, which is currently a bottleneck for their system.

**Storage Capacity**

- Yasir mentioned that the SWG have been increasing server capacity due to demand, with some servers now at 50 terabytes. However, moving data between servers can be time-consuming as there is no backup elsewhere.

**Server Distribution**

- Yasir shared that the storage services are well-distributed around the world with no clustering in one place or three places (which would be risky).

**Performance Issues**

- Performance issues related to timeouts when downloading or uploading content, which was being investigated by BWG.

**Capacity Planning**

- The team monitors load coming into each server closely and tracks growth trajectory daily.- They keep adding more workers with more capacity as needed while monitoring how much percentage of a server has been loaded up recently.

**Hiring Plan**

- Yasir suggests that they will be hiring at least once or twice a month in the coming months based on the current trajectory.

**Server Locations**

- Codefikeyz asks about server locations and why there are no servers in Africa. Yasir explains that server providers look for cost-effectiveness and they cannot allow people to cluster in one place.

**Server Provider Requirements**

- The process of becoming a server provider is explained by Yasir. Anyone can apply, but preference is given to those who have skills and are active members of the community. The current requirement for a server is around 500 GB of Nvme storage and 50 TB of HDD storage.

**Monitoring Servers**

- Yasir explains that daily maintenance involves monitoring servers regularly, checking logs for any issues or errors, investigating logs when necessary, upgrading components periodically (once every month or two), etc. He also notes that basic Linux knowledge is required to become server provider.

**Future Scaling Plans**

- Yasir discusses future scaling plans with regards to capacity as well as performance since heavy usage could cause delays/busy periods if not managed properly. This issue is currently being investigated so it can be addressed before it becomes problematic at scale.

**End of Session**