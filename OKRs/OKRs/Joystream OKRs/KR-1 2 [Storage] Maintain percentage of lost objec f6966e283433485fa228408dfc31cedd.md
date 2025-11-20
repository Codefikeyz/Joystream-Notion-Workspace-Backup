# KR-1.2 [Storage] Maintain percentage of lost objects 0%. Maintain percentage of unaccepted objects < 1%. Maintain a replication rate of not lower 2 for all objects. Maintain an average node availability of 99.9%

Assignee: Storage WG
Parent item: [2024 Q1] O-1-1 Improve Joystream as a Video Platform (%5B2024%20Q1%5D%20O-1-1%20Improve%20Joystream%20as%20a%20Video%20Platf%2070ee7f8b6c2d401195de1f1348b1454a.md)
Progress: ◾️◽️◽️◽️◽️◽️◽️◽️◽️◽️10%
Status: At risk ⚠️
Last Updated: March 7, 2024
Last edited time: June 18, 2024 6:31 PM

- Introduce tools to indicate the operational status of a node
- Implement SubSquid
- Conduct periodic benchmarking of the storage infrastructure
- Establish authentication between Argus and Colossus, including storage authentication on the consumer side: design specification which will cover user download, and node-to-node authentication *(previous work “[**Standardise Argus access policy signals in metadata**](https://github.com/Joystream/joystream/issues/4332)”)*
- Add support for block storage (prototype)
- Fix Colossus timeout issues

21 Feb 2024

**Agreed actions in the order of priority**

- Failed Uploads → 
Status: In progress, should be top prio.
Update on failed uploads: object uploads from misc locations to all operators and benchmarking is required to be added to the current process. Current understanding: Colossus serves 500, but we are not sure if that is caused by the bug in the code. 
****Action for failed uploads: collect data and report on failed uploads events: client location, node location, object details, configuration details and whatever can help us find the pattern.
- Action: Yassir will create a plan (notion page/ forum post) which encapsulates the detailed list of activites that can be taken to reduce the costs, the estimation of how much the costs would go down and impact.  
Status: In progress, should be second prio.
- Maintain a replication rate of 4 for all objects → 
- Action reqd: research the feasibility of reducing replication layer further  (2 or 3) and evaluate impact on costs. (Potentially: S3 bucket to colossus and run colossus node that runs all the buckets but does not accept objects) → Not started, should be third prio. 
Status: On track
- Implement SubSquid → 
Update: Rolling it out now for single node, after the tests are good rolling to all. On track.
- Conduct periodic benchmarking of the storage infrastructure → 
Status: On track. 
Update: it was never done
Action: we need a monthly update on benchmarking from the lead. A paragraph with “everything is fine or there are problems + screenshots from dashboard”. End of Feb for the first one, End of March for the final one.
- Add support for block storage (prototype) → 
Update: Enables deep freeze layer and reduction of replication factor.
Status: Not started. Blocked.
- Introduce tools to indicate the operational status of a node → 
- Update: reworded to 
”Introduce ability to set node operation status in Colossus and Argus” (awaits Zeeshan’s deployment of this feature, potentially builders can work on this - TBC). Blocked now.
- Establish authentication between Argus and Colossus → Not started. Blocked.
- Fix Colossus timeout issues → **Fixed**

### 7 March 2024

We are failing "Maintain percentage of lost objects 0%" due to the upload failure.

### 8 March 2024

- Per yyagi (WG lead) things are still being investigated
- We are failing upload rate due to a bug, it is being investigated but the root cause is still not understood
- 99.9% availability is not currently being met
- OKR changed as per approved proposal ([https://pioneerapp.xyz/#/proposals/preview/814](https://pioneerapp.xyz/#/proposals/preview/814))

April 15

- Percentage for the the unaccepted objects was 1.88% which below the target
- RE Lost objects: Still under investigation to set baseline for measurement
- The 99.99% of node availability is met by the end of Term 31

### April 30

- Maintain percentage of lost objects 0%.
    - Score 0.0 (fixed in latest release )
- Maintain percentage of unaccepted objects < 1%.
    - Score 0.0 (fixed in latest release + system doesnt properly mark the accepted/unaccepted objects)
- Maintain a replication rate of not lower 2 for all objects. Maintain an average node availability of 99.9%
    - Score 1.0
    

Score: 50%

Note: Maintain an average node availability  → better name Maintain an average storage system availability