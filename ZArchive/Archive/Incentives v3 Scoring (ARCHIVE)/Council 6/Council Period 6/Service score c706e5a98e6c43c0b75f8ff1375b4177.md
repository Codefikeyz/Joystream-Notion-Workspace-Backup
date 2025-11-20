# Service score

Group: Distributors
Score Status: Ready for review
Score: 1
Attributes: Grade, Spot Check, Subscore
Reports Gathered: No
Grade Name: SERVICE_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/distributors-score#service_score
Parent Score: Distributor Score (Distributor%20Score%20998f4998e98247aab958933b3ca7bd9e.md)
Score Type: Main Score
Spot Check Completed: No

Spotcheck 1 of 1:

| avg_download_ratio_i | 25.13342004 |
| --- | --- |
| average duration | 195.39 |
| average download time | 7.774111111 |
| **min_download_ratio_i** | 7.19834792 |
| lowest playtime | 366 |
| download time | 50.845 |
| **avg_buffering_i** | 1.398422222 |
| **max_buffering_i** | 2.708 |

```markdown
	avg_download_ratio_score = Zigma[max(avg_download_ratio_i-1,1)]/i
= 1
  min_download_ratio_score = Zigma[max(min_download_ratio_i-0.5,1)]/i
= 1
  avg_buffering_score = Zigma[max((5-avg_buffering_i)/3,1)]/i
= max((5 - 1.39/3),1) = 1
  max_buffering_score = Zigma[max((10-max_buffering_i)/6,1)]/i
= max((10 - 2.71/3),1) = 1

  # finally
  service_score = 0.25*(avg_download_ratio_score + min_download_ratio_i + avg_buffering_i + max_buffering_i)
= 1
```