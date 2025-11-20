# Research Score

Group: Distributors
Attributes: Group Specific Scores, Subscore
Score: 0
JSG Grading Status: Completed
Grade Name: RESEARCH_SCORE
Spot Check Completed: No

Nothing appears to have been done.

---

To evaluate a system like this, we need to make sure the individual node logs are available, and useful.

**`DEFAULT_LOGGING`** Review what is currently being logged by a distributor node, for each configurable `log-level`.
 Describe what information it provides, and in what way it can be used 
to improve the data in the current report, or what new statistics can be
 derived from it.

**`ELASTIC_LOGGING`** In the `config.yml` file `elastic` is commented out. Look into the codebase/documentation, and:

- deploy a server to act as the endpoint
- have a distributor node or two report to it, and compare the resource consumption before/after (a couple of times)
- make it public, so it can be used to debug and collect data
- create a guide that explains how to set it up, and use it to look at the logs

Note that the storage providers will have a similar task - consider collaborating.

### 

### Scoring Calculations

Jsgenesis will assign a score in the range [0,1] based on:

- The quality of the report
- The quality of the guide
- The amount of nodes that connected to the server