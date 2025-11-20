# Research Score

Group: Storage
Attributes: Group Specific Scores, Subscore
Score: 0.9
JSG Grading Status: Completed
Grade Name: RESEARCH_SCORE
Spot Check Completed: No

**Research Logging**

To evaluate a system like this, we need to make sure the individual node logs are available, and useful.

**`DEFAULT_LOGGING`** Review what is currently being logged by a storage node, for each configurable `log-level`.
 Describe what information it provides, and in what way it can be used 
to improve the data in the current report, or what new statistics can be
 derived from it.

**`ELASTIC_LOGGING`** There is an option for the storage node to run with `-e URL`, meaning logs, with configurable verbosity can be uploaded to an endpoint.

- deploy a server to act as the endpoint
- have a storage node or two report to it, and compare the resource consumption before/after (a couple of times)
- make it public, so it can be used to debug and collect data
- create a guide that explains how to set it up, and use it to look at the logs
- use the most verbose log level, and IF that `LOG_LEVEL` differs from what was found in `DEFAULT_LOGGING`, outline what is added

---

```markdown
Jsgenesis will assign a score in the range \[0,1] based on:

* The quality of the report
* The quality of the guide
* The amount of nodes that connected to the server

**ELASTIC_LOGGING -> 0.8
(No guide)
DEFAULT_LOGGING -> 1.0**
```