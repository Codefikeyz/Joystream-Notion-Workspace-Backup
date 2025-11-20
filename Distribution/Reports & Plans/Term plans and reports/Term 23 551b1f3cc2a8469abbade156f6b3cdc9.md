# Term 23

## Term 23 plan

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 1 | 2098 | `0x2bc` | operator |
| 2 | 458 | `sieemma` | operator |
| 8 | 4236 | `Deathix` | operator |
| 10 | 2502 | `adovrn` | operator |
| 12 | 2233 | `klaudiusz` | operator |
| 15 | 2233 | `klaudiusz` | monitoring operator |
| 16 | 2233 | `klaudiusz` | lead |
| 17 | 2137 | `kalpakci` | operator |
| 18 | 12757 | `p0k` | operator |
| 19 | 11765 | `spoonbender` | operator |

### 2. **Group budget**

**JOY/USDT EMA30: 0.029** USDT

| **Item** | **USDT** | **JOY** | **Comment** |
| --- | --- | --- | --- |
| Operator salaries | $250 * 7 = $1750 | 8,620.69 JOY * 7 = 60,344.83 JOY |  |
| Monitoring operator salary | $75 | 2,586.21 JOY |  |
| Lead salary | $1,190.16 | 41,040 JOY |  |
| Lead server compensation | $25 | 862.07 JOY |  |
| Total Spending | $3,040.16 | 104,833.11 JOY |  |

### 3. **Group tasks**

1. Roll out request tracing to all operators and analyze the data.
2. Deploy latest Argus version to all operators.
3. Get more results for benchmark app.

---

## Term 23 report

### 1. **Group composition**

| Worker ID | Member ID | Member handle | Role |
| --- | --- | --- | --- |
| 1 | 2098 | `0x2bc` | operator |
| 2 | 458 | `sieemma` | operator |
| 8 | 4236 | `Deathix` | operator |
| 10 | 2502 | `adovrn` | operator |
| 12 | 2233 | `klaudiusz` | operator |
| 15 | 2233 | `klaudiusz` | monitoring operator |
| 16 | 2233 | `klaudiusz` | lead/operator |
| 17 | 2137 | `kalpakci` | operator |
| 18 | 12757 | `p0k` | operator |
| 19 | 11765 | `spoonbender` | operator |

### 2. Group budget

**JOY/USDT EMA30: 0.029** USDT

| **Item** | **USDT (planned)** | **USDT (actual)** | **JOY (planned)** | **JOY (actual)** |
| --- | --- | --- | --- | --- |
| Operator salaries | $250 * 7 = $1750 | $1750 | 8,620.69 JOY * 7 = 60,344.83 JOY | 60,344.83 JOY |
| Monitoring operator salary | $75 | $75 | 2,586.21 JOY | 2,586.21 JOY |
| Lead salary | $1,190.16 | $1,190.16 | 41,040 JOY | 41,040 JOY |
| Lead server compensation | $25 | $25 | 862.07 JOY | 862.07 JOY |
| Total Spending | $3,040.16 | $3,040.16 | 104,833.11 JOY | 104,833.11 JOY |

### 3. Group tasks

> Roll out request tracing to all operators and analyze the data.
> 

Done.

> Deploy latest Argus version to all operators.
> 

Done.

> Get more results for benchmark app.
> 

Done. DWG coordinated with HRWG and MWG to create a raffle and promotional campaign to get more benchmark results. 113 results were collected during the term, and a bit more will most likely be collected next term. This can be tracked here: [https://kibana.joyutils.org/app/dashboards?auth_provider_hint=anonymous1#/view/5feb0da0-751f-11ee-a4a5-731d19b33886?_g=(refreshInterval%3A(pause%3A!t%2Cvalue%3A60000)%2Ctime%3A(from%3Anow-15d%2Cto%3Anow)](https://kibana.joyutils.org/app/dashboards?auth_provider_hint=anonymous1#/view/5feb0da0-751f-11ee-a4a5-731d19b33886?_g=(refreshInterval%3A(pause%3A!t%2Cvalue%3A60000)%2Ctime%3A(from%3Anow-15d%2Cto%3Anow)))

### 4. Extra Items

1. Deployed improved setup for collecting system-level metrics of DWG servers: [https://share.cleanshot.com/5QLkXhFj](https://share.cleanshot.com/5QLkXhFj)
2. Some Elasticsearch maintenance was required. With our Elastic cluster collecting logs and traces from all storage and distribution operators, one of the cluster nodes was running out of space. New server was rented to replace this node. Also improvements to the cluster were made so we can ensure its high availability and data retention.
3. DWG monitoring script was deployed via cloud to few additional locations. Currently we ping operators from 7 locations across the globe.
4. Collaborated with SWG on topic of lost objects and objects that distributors couldn’t fetch from storage operators.
5. Report based on benchmark test results was started.