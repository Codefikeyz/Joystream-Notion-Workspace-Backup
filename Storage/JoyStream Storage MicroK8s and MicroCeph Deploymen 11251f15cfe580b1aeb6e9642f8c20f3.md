# JoyStream Storage MicroK8s and MicroCeph Deployment

# 

## Overview

The aim of the project is to prototype the storage component deployed using Kubernetes and Ceph. The main idea behind this is to provide an overall solution that is easy to implement and maintain

## Scope

The project will focus on providing storage to back the storage component for joystream application. This is includes:

1. PoC of the solution - Setting up the solution on already existing and connected infrastructure
2. Documentation
3. Possibly write automation for future deployments if possible ( TBD )

**Assumptions**

•    Storage Application is already dockerized.

•    Infrastructure will be provided this includes but not limited to servers with OS installed, networking etc..

•    3 servers will be provided.

## Solution

Kubernetes will be setup on one server using MicroK8s, this cluster will run:

1. Storage application pods:
    1. storage
    2. joystream-node
    3. squid-graphql-server
    4. squid-processor
    5. squid-db
2. Monitoring pods/custom resources
    1. grafana
    2. prometheus
    3. alertmanager
    4. node_exporter
    5. grok_exporter
    6. cadvisor
3. Nginx ingress controller.

Ceph will be setup on the other two servers using MicroCeph to make a Ceph cluster. The k8s cluster and the Ceph cluster will be connected using Rook, this way the storage pods can request for storage from the Ceph cluster using PVCs.

Current build: [https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/NodeSteup](https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/NodeSteup)

## Steps

1. Planning
2. Setup Kubernetes cluster MicroK8s 
    1. Networking
    2. Monitoring
    3. Basic Configuration 4. Security
3. Setup Ceph Cluster - 
    1. Networking 
    2. Monitoring 
    3. Basic Configuration 
    4. Security
4. Connect the two cluster
    1. Configure Rook
5. Write and test manifests/helm charts that request for and consume storage from Ceph
6. Automation ( use Ansible to perform steps 2, 3 and 4 ).

## Proposed Tech

- Micro8s [https://microk8s.io/tutorials](https://microk8s.io/tutorials)
- Rook [https://rook.io/docs/rook/latest-release/Getting-Started/intro/](https://rook.io/docs/rook/latest-release/Getting-Started/intro/)

## Deliverables

1. Kubernetes Cluster
2. Ceph Cluster
3. Working Joystream storage node
4. Ansible playbook
5. Full Documentation in Joystream community Github

## Acceptance Criteria

Joy stream storage component deployed on a kubernetes cluster, which must be backed by storage provided by a Ceph cluster.

1. Joytream storage component deployed on a kubernetes cluster
2. Application requests for and consumes storage from the Ceph cluster
3. Working Ansible playbook
4. Full documentation 

## Testing

TBD

## Project Costs

| S/N | Step | Estimated Time in Hours |
| --- | --- | --- |
| 1 | Planning | 10 hrs |
| 2 | Setup Kubernestes cluster | 25 hrs  |
| 3 | Setup Ceph cluster | 25 hrs  |
| 4 | Configure Rook | 15 hrs  |
| 5 | Write kubernetes manifests | 5 hrs  |
| 6 | Automation (Ansible) | 15 hrs  |
| 7 | Documentation | 15 hrs  |
|  | Total  | 120 hrs  |

The time estimates are just that. They are merely guidelines it could be more or less.