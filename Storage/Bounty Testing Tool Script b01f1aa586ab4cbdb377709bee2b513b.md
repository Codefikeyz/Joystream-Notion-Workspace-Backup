# Bounty Testing Tool/Script

- **Title**

Bounty Testing script

- **High level summary and purpose**

 Tool/script that allow the admin to testing the following for each node:

- Reachability
- HTTP connection
- Upload
- **Time estimate to complete, assuming some relevant skills.**

Rough estimation is 20 hours.

- **Detailed scope of work, relevant for either a specific part of the working group score, or more general**

The tool tests:

1. The server is reachable
2. The storage server is listening
3. upload a small file to server a check the result

The tools should output a table:

1. Worker ID
2. Worker Handle
3. Bucket number
4. Bucket URL
5. Bucket IP address
6. File size
7. Upload time in MS
8. result 
9. Errors if any

The tools should be able to provide result for one node, multiple or all.

- The tools should query each operational bucket.
- The preferred programming language is python.

**Results should include** 

- Command line tools to test nodes health
- Short guide of how to set and use.

Storage Lead:    yyagi

Member ID:      3098

Feel free to write in the Discord channel #storage-provider

- **Reward**

400,000 tJOY/hour of work ($1866 in mainnet JOY)