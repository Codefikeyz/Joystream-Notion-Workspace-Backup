# OKR Q1 (revised 08 Feb  2024) (1)

**Comments**

- [Q1 OKR discussion](https://pioneerapp.xyz/#/forum/thread/741)
- KR statuses: 🟢 fully agreed,  🟡 required further discussions

### **O-1-1 Improve Joystream as a Video Platform**

- **KR-1.1 [Distributors]  Ensure median bandwidth > 20 Mbps and median TTFB < 350 ms for all deployment locations (*across multiple tests*).**
    
    (1) Deployment locations: N. Virginia, Sao Paolo, Madrid, Mumbai, Jakarta, Seoul.
    (2) Cached assets only consider for testing
    (3) Synthetic tests details
    
    [https://joystream.notion.site/CDN-Performance-standard-79000919c67d4aba8fa90541cfee9f93](https://www.notion.so/CDN-Performance-standard-79000919c67d4aba8fa90541cfee9f93?pvs=21)
    
    - Improve geographic node coverage by hiring workers for South America + Africa
    - Improve benchmarking process by reviewing the code (not sure eg if the TTFB includes DNS resolution time + handshakes time ) and maybe deploy scripts for more locations for the ping tool
    - Investigate Argus node selection by Orion and Atlas
    - Investigate usage of CloudFlare workers for improved bandwidth
    - Improve CPU usage of Argus node (this is to be attained by siding Argus with a bespoke squid and reducing state cleanup to once a week). This should lower latency for video requests
    - Collect data from end-users of apps (Gleev) to see perceived performance
- **KR-1.2  [Storage]  Maintain percentage of lost objects 0%. Maintain percentage of unaccepted objects < 1%. Maintain a replication rate of 4 for all objects. Maintain an average node availability of 99.9%**
- Introduce tools to indicate the operational status of a node
- Implement SubSquid
- Conduct periodic benchmarking of the storage infrastructure
- Establish authentication between Argus and Colossus, including storage authentication on the consumer side:  design specification which will cover user download, and node-to-node authentication *(previous work “[**Standardise `Argus` access policy signals in metadata**](https://github.com/Joystream/joystream/issues/4332)”)*
- Add support for block storage (prototype)
- Fix Colossus timeout issues
- **KR-1.3**  **[Builders]  Atlas SDK: development of functional design specification**

### **O-1-2 Improve Joystream as a Blockchain Project**

- **KR-2.1 [Council] Average block time is less than 6.1s**

### **O-1-3 Improve Joystream DAO Governance**

- **KR-3.1 [HumanResources] Conduct 2 anonymous surveys to understand whether DAO workers are satisfied with governance and working conditions.** Use the similar survey template as was used in Q4 2023
    - Create a council scoring system (prototype)
    - Create a WG scoring system (prototype)
- **KR-3.2 [Builders] Pioneer Validator dashboard** Add validator module on Pioneer
- **KR-3.3 [HumanResources] Develop prototype of council and lead scoring system**
- **KR-3.4 [HumanResources] DAO pay structure**

### **O-1-4 Enhance Joystream user adoption**

- **KR-4.1 [Marketing] Joystream is listed on at least 2 more CEX:** Achieve social media metrics required for exchange listing, Execute listing with DAO provided funds
- **KR-4.2 [Marketing] At least 25 new Joystream-related review videos targeted at crypto audiences are posted on Youtube**
- **KR-4.3 [Marketing] At least 3 new interviews with Joystream team are conducted and published**
- **KR-4.4 [Marketing] Reach 32,000 non-empty channels and 1,400,000 non-spam videos on Joystream by the end of Q1**
- **KR-4.5 [Marketing] Onboard 10 Marketing Ambassadors**
- **KR-4.6 [HumanResources] Conduct NPS survey for content creators 2 times per quarter.** Use the similar survey template as was used in Q4 2023
- **KR-4.7 [HumanResources] At least 5 community events or workshops are organized aimed at/for content creators during the quarter. The total views of the event recordings should not be fewer than 500 views across all platform for all 5 videos.**
- **KR-4.8 [Marketing] Achieve a 20% increase in total social media impressions compared to the previous quarter**
    - Create social media marketing strategy
    - Create educational content/infographics and post regularly
- **KR 4.9 [Content] At least 5 gold+ tier creators have created a creator token**