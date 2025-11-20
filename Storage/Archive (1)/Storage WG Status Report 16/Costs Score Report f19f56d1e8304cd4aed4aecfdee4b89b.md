# Costs Score Report

<aside>
💡 It seems the COST_SCORE appeared from the fact that we hired more people that we really needed (I informed about that  Council many times). So COST_SCORE is basically raises a question, why we have so many people maintaining costly hardware taking into account that this extra capacity is not really needed.

</aside>

<aside>
💡 Improvement of COST_SCORE may affect WG_OPPORTUNITY SCORE and vice versa

</aside>

### **Current Costs**

[Current costs](Costs%20Score%20Report/Current%20costs%2042d0dd7a129f47a38b2643ec1202c157.csv)

### Two basic options:

- decrease the number of storage workers
- decrease the average cost per one worker

### 

### (1) **Decrease average costs per one worker**

**This can be done without impacting other scores**

For every worker we can downgrade servers configs, as a result decrease their cost 

- Use servers with lower storage capacity
    - Lets assume
        - number of workers=15,
        - replication rate=5
        - total storage volume= 1000GB
    
    We can have 15 buckets each of size 333GB that will fit the requirements. Having some extra capacity for the growth, each storage node can have 600-800GB of space and that will be enough for now.  Moreover soon all storage objects - or almost all- will be reseted. So we will need even less storage capacity.
    
- Use servers with lower CPU configs
    - we can have the following config
        - many cheap low grade  VPS
        - few high grade dedicated servers
    - low grade  VPS will use Query Nodes and Joystream Node endpoints from high grade dedicated servers, for example for each 3 VPS we can have 1 high grade dedicated server.
    - This will allow to further decrease our costs

Pros: 

- Hard to implement
- This will have no effect on WG_OPPORTUNITY SCORE

Cons: 

- This may have small negative effect on SYSTEM SCORE

### (2) **Decrease number of storage workers**

**This can be done with impacting other scores**

We can decrease the number of workers to 5-7 people.

<aside>
💡 Together with `SYSTEM_SCORE`a replication of channels to 5 SP each should be a safe option (leaving 2 functional nodes when up to three go down).

</aside>

Pros: 

- Easy implementation

Cons: 

- This will probably negatively affect WG_OPPORTUNITY SCORE

### Conclusion

- I would suggest to *not* fire people that we have recently hired
- On the other hand we need to *stop* hiring new people or at least significantly slow down the process (we don’t really need so many people on the road to mainnet: it makes the system less stable and harder to manage)
- Also, we can use approach of *Decreasing average costs per one worker*, that i described above
- If people don’t want to re-configure their servers for cheaper ones, we can leave these high grade servers and use them as Query Node and Joystream Node endpoints
- **And, probably, we need to think about the following:**
    - If people agree to maintain high grade servers for the rewards that they are getting now,  should we really ask them to start renting lower grade servers which most probably will lead to a worse quality of work for the whole system?
    - Do we still believe that total costs really a problem? We need to consider the fact that since the launch of new Testnet (end of July), we will re-hire people again, and we actually can hire them in a lower amount