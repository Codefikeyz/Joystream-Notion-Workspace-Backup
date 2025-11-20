# README (hover + open) ℹ️

**Context**
JSG team set up an internal tool to monitor the availability Atlas and Pioneer FE applications as well as BE services involved in running them.

**Services encapsulated**
Atlas prod
Pioneer prod

Orion - Atlas Backend

Query Node

Faucet - service involved in creating new memberships, allocating small initial funds of Joy tokens to help create new accounts.

Avatar Service used jointly by Atlas and Pioneer

**Public Dashboard**

[Checkly | Active Monitoring for Dev & Ops Teams](https://app.checklyhq.com/)

**Monitoring tool used**
Checkly

[Checkly | Active Monitoring for Dev & Ops Teams](https://app.checklyhq.com/)

Justification of the choice can be found in this issue

[Atlas infrastructure monitoring · Issue #3297 · Joystream/atlas](https://github.com/Joystream/atlas/issues/3297#issue-1395938531)

**Responsible Engineers**

| System | Engineers |
| --- | --- |
| Atlas Prod |  Bartosz, Rafal, Klaudiusz |
| Orion (Atlas BE) | Rafal, Klaudiusz |
| Avatar Service  | Bartosz, Rafal, Klaudiusz |
| QN | Zeeshan, Bartosz, Theo |
| Faucet | Theo, Mokhtar |
| Pioneer Prod | Theo |

**SLA**

Will be clarified later by @Martin 

**Alerts Configuration**

Alerts posted if service availability checks are failed from the first attempt. Fail means failed API call or Browser check is detected with a time delta of 15min for FE apps, 5min for BE services and 10min for QN.

Alerting also includes SSL certificate expiration 30 days before it is due.

****Alerting is done via external channels: email notifications, JSG teams slack channel posts and SMS notifications to responsible engineers.

Details can be found here:

[Checkly | Active Monitoring for Dev & Ops Teams](https://app.checklyhq.com/alerts/settings)