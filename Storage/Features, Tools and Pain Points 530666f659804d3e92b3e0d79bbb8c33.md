# Features, Tools and Pain Points

## Pain Points

- [ ]  Failed Objects are currently market as accepted
    
    Currently there are lots of objects that failed the upload but the QN have them with accepted flag.
    
- [ ]  If one of the buckets assigned to bag is full, the bag cannot upload
    
    I  think e can assign min and max threshold for replication, and as long as the min is met upload continue.
    
- [ ]  replication creating a lot 4xx error due to randomly looking for objects
    
    Since the QN has which bucket accepted the object. may be initially only replicate from it.
    

## Features

- [ ]  Node Operational Status
- [ ]  Metrics collection
- [ ]  Auto set bucket limits: Worker node inject the auto detected folder size and number of files (according to some math). Lead can can use the onchain data as default or others.
- [ ]  Dynamic server monitoring: Severs already replicate from each other, may be we can come with a scoring scheme to indicate other servers reachability; for example if 3 servers failed to reach the server then the server state is changed not accessible then we set a back-off timer.  Change of state is collected as metrics.
- [ ]  Add support for block storage and object storage
- [ ]  ~~Storage sharding: sharding files broken at equal sizes will make the usage of bucket uniform and also makes retrieving the objects faster.~~
- [ ]  Authentication between Argus and Colossus

## Tools

- [ ]  Rebalancing bags: command auto move bags from one bucket to other to bucket to balance used capacity in buckets.
- [ ]  Set salaries
- [x]  Lost objects