# Bounty Elastic Search Development

- **Title**

Bounty Elastic Search Development

- **High level summary and purpose**

Finish setting up of Elastic Search for the Storage WG purposes. As a result, all Storage Nodes reporting which now is made through external data server should be accessible via Elastic Search. All guidlines on how to set up Elastic Search and Storage nodes should be finalized.

The LOGGING_SCORE [[https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#logging_score](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#logging_score)] should be completed.  

- **Time estimate to complete, assuming some relevant skills, but little to no experience with Joystream or the working group**

Rough estimation is 20 hours.

- **Detailed scope of work, relevant for either a specific part of the working group score, or more general**

Participant should revise guides for the Elastic Search. Participant should update or create guides for the Elastic Search-relating processes including:

- Deploying and using the server
- Setup and configurations
- Extracting and parsing the data

Participant should set up Elastic Search to be able to collect all Storage Reporting data that cannot be obtained via GraphQL, including:

- Failed upload objects list
- Nodes’s traffic consumption

Some of work was initiated but not hasn’t been finished yet. See [https://github.com/yasiryagi/elasticsearch-docker/tree/master/client](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client), [https://github.com/yasiryagi/elasticsearch-docker/](https://github.com/yasiryagi/elasticsearch-docker/tree/master/client), [https://kibana.joystreamstats.live/app/dashboards](https://kibana.joystreamstats.live/app/dashboards)

**Results should include** 

- Guides on how to set up Elastic Search from scratch,
- Guides on how to configure Storage dashboard
- Guides for nodes operator how to transfer information to the  Elastic Search
- Working Elastic Search server ( configured ES, configured Dashboards, configured Storage WG servers [at least 5 servers])
- **Discord handle and `memberId` of a worker (or the Lead) WG to act as the oracle for the bounty**

Storage Lead:      **xJames#8645** 

Member ID:         **2098**

Feel free to write in the Discord channel #storage-provider

- **Reward**

100,000 tJOY/hour of work ($200 in mainnet JOY)