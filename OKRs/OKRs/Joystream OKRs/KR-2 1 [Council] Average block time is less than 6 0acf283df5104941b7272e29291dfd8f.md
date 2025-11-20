# KR-2.1 [Council] Average block time is less than 6.1s

Assignee: Council
Parent item: [2024 Q1] O-1-2 Maintain Security of the Joystream Blockchain (%5B2024%20Q1%5D%20O-1-2%20Maintain%20Security%20of%20the%20Joystream%203621c17edff84302bf2819d79618dadf.md)
Progress: ◾️◾️◾️◾️◾️◾️◾️◾️◽️◽️80%
Status: On track ✅
Last Updated: March 8, 2024
Last edited time: April 30, 2024 10:30 AM

### 21 Feb 2024

What will happen if error occurs

1. the estimation of the dates will shift a lot
2. and the network will become slower

Todo

- Forum post to discuss the error is required
- Improve the naming of OKR

### 8 March 2024

- Unlikely to have exceeded `6.1s`
- Validator count was decreased a few days ago to try and mitigate an increase in sporadic blocktimes as the average blocktime had crept up slightly, but this appears to have not had the desired effect and it is likely that the sporadic 12s blocktimes (indicating a missed block by a validator) may be due to underspecced validator hardware. Telemetry shows
- According to Klaudiusz we are getting close to breaching the 6.1s number during this council term so far—however the average over the entire quarter is unlikely to have breached the number.
    - average this term = 6.066s
    - average this quarter = 6.03s
- Tomato has been in contact with validators to try and get them to run system benchmarks, however validators are resistant to run on higher quality hardware due to the costs involved and the current low rewards to validators.
- It is unclear how this can be addressed in the future, but seems like an issue that should be investigated more thoroughly.

### 30 April 2024

Score: 100%

Check Klaudiusz script