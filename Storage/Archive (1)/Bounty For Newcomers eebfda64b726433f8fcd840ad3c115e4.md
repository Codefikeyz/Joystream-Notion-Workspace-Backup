# Bounty For Newcomers

## Bounty #1

**Short description:** Change the Reporting system: [Update the script](Storage%20Node%20Reporting%20Script%20fbf17c27b86c4e5d87b8f9023a3b1233.md) to post data on the [Elastic Search endpoint](https://kibana.joystreamstats.live/app/dashboards#/list) instead of FTP server that we use now. 

**Purpose:** 

(1) ****We will use the one unified reporting dashboard 

(2) We start using the Grafana + Elastic Search system for the reporting. This is  something that JSG is really looking for 

**Requirements:** 

- Ask l1dev for credentials for the Elastic Search
- Update reporting script (make a new page on notion with guidelines)
- Configure Dashboards on the Elastic Search that will provide the following data
    - total traffic consumption of the each server
    - total traffic consumption of the Storage Node for each server
    - list of Storage Objects on the server
    - speed test for the Storage node