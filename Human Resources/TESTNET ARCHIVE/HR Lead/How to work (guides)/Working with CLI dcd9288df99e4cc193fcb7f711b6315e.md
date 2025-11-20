# Working with CLI

**Detailed instructions for using the CLI ⬇**

[joystream/cli at carthage · Joystream/joystream](https://github.com/Joystream/joystream/tree/carthage/cli)

**The most commonly used commands:**

`joystream-cli working-groups:overview --group=humanResources` - group overview.

`joystream-cli working-groups:fillOpening -g humanResources --openingId=**1**` - Hire worker. You need to specify the id of the opening.

`joystream-cli working-groups:evictWorker **1** --group=humanResources` - Fire worker. Instead of "1" insert the worker's id.

`joystream-cli working-groups:updateWorkerReward **3** **4** --group=humanResources` - Set salary. The first number is the worker id. The second number is the number of JOY/per block.

`joystream-cli working-groups:createOpening --group=humanResources` - Create an Opening.

`joystream-cli working-groups:createOpening -i **temp.json**` - Create an openning via a json file. You need to specify the file name.

**Integrator opening json example:**

[temp.json](Working%20with%20CLI/temp.json)

**Lead Deputy opening json example:** 

[temp2.json](Working%20with%20CLI/temp2.json)

[](Working%20with%20CLI/Untitled%2004cd409f4e59472fb3a2476bbc2e9569.md)