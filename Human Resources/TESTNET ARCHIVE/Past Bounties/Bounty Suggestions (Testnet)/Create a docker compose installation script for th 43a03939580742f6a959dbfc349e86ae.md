# Create a docker compose installation script for the storage node

Status: Ready to use
Reward tJOY: 500000
Takes time: ~24 h
Specification: Storage
Submited by: Yasir

[Storage node docker and installation script](https://www.notion.so/Storage-node-docker-and-installation-script-b3013931a9d942958ac5a7e09bc9ef0e?pvs=21) 

---

Description:

!! WARNING !! This BOUNTY IS CREATED FOR ONE USER ONLY (for ). The work of other users will not be appreciated.

Allow new member to set up storage node without any strict requirements & deadlines. Give a new member understanding how to work with node.

- **High level summary and purpose**

 Create a docker compose installation script for the storage node 

- **Time estimate to complete, assuming some relevant skills, but little to no experience with Joystream or the working group**

Rough estimation is 40 hours.

- **Detailed scope of work, relevant for either a specific part of the working group score, or more general**
- The result should include:
- Joystream node
    - Docker Joystream node
    - Docker compose setup
- Storage node
    - Storage docker
    - Docker compose setup
- Nginx docker
    - Docker compose setup
    - handle traffic to: Storage node, Query node, Joystream node
- prometheus
    - node-exporter
    - cadvisor
    - alertmanager
- Orchestration Ansible playbook to install (optionally script)
    - Nginx
    - Joystream node
    - Query node
    - Storage node
    - prometheus
        - node-exporter
        - cadvisor
        - alertmanager

Storage Lead:    yyagi

Member ID:      3098

Feel free to write in the Discord channel #storage-provider

**Actions to do after bounty is complete:** Contact current Storage workgroup lead to validate node set up. If lead approves your setup your bounty can be treated as successful.

When you submit your work, you need to write that you have contacted the lead of the group.