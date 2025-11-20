# Storage Lead Daily Report - Period 1

# Storage Lead Report

*Full report on tasks performed by Storage WG Lead*

# **Carthage pre-release work**

## Docs

[Lead docs](https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/leader) 

[Team detail](https://docs.google.com/spreadsheets/d/1Zu_RIJ1rAChJx637u7Ua7A8lVrT6TjigXdTWIRxxRl8/edit#gid=0)

## Nov-26-2022

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |

**Performed tasks:**

- Initial storage setup
- Setup Lead server
- Hired two workers
- Created 3 new buckets
- One bucket accepting new bags.
- Recruiting 3 more workers
- Working with the recruit to accrue and setup servers.
- Documenting setup and updating documentation

**Executed commands:**

### Set env

```
 yarn joystream-cli api:setQueryNodeEndpoint
 yarn joystream-cli api:setQueryNodeEndpoint
 yarn joystream-cli account:import  --backupFilePath  /root/keys/storage-role-key.json
 yarn joystream-cli working-groups:setDefaultGroup -g storageProviders
 yarn joystream-cli working-groups:overview -g=storageProviders
```

### Setup Storage default

```
 yarn storage-node leader:update-voucher-limits -s 200000000000 -o 20000 -k /root/keys/storage-role-key.json
 yarn storage-node leader:update-voucher-limits -s 200000000000 -o 20000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/keys/storage-role-key.json xxxxxxxx
 yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/keys/storage-role-key.json -P xxxxxxxx
 yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Creating opening

```
 yarn joystream-cli working-groups:openings
 yarn joystream-cli working-groups:createOpening -o /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Deputy_Leader.json -k /root/keys/storage-role-key.json -a 1 -p xxxxxxxx
 yarn joystream-cli working-groups:createOpening -o /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Deputy_Leader.json
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Deputy_Leader.json
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
 yarn joystream-cli working-groups:createOpening
 yarn joystream-cli working-groups:createOpening  -o openinh_template.json
 yarn joystream-cli working-groups:createOpening  -o opening_template.json
 yarn joystream-cli working-groups:createOpening  -o opening_template.json
```

### Setup Storage default

```
 yarn storage-node leader:update-bag-limit -l 10 -k /root/keys/storage-role-key.json
 yarn storage-node leader:update-bag-limit -l 10 -k /root/keys/storage-role-key.json  -p xxxxxxxx
 yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-voucher-limits -s 200000000000 -o 20000 -k /root/keys/storage-role-key.json
 yarn storage-node leader:update-voucher-limits -s 200000000000 -o 20000 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Creating opening

```
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Deputy_Leader.json
 yarn joystream-cli working-groups:cancelOpening 1
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Deputy_Leader.json
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
 yarn joystream-cli working-groups:cancelOpening 3
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
 yarn joystream-cli working-groups:overview
```

### Creating bucket for worker 0 (lead)

```
 yarn storage-node leader:create-bucket -i 0 -n 20000 -s 1500000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:create-bucket -i 0 -n 20000 -s 200000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-bucket-status -i 0 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Setting up the server

```
 yarn run storage-node operator:accept-invitation -i 0 -w 0 -t 5CPhA9RkPnykLxGy1JVy1Y4x9YPSYq9iq48NAMzoKXX9mLG8 --password=xxxxxxxx -k /root/keys/storage-role-key.json
 yarn run storage-node operator:set-metadata -i 0 -w 0 -j ~/root/joystream/metadata.json --password=xxxxxxxx -k /root/keys/storage-role-key.json
 yarn run storage-node operator:set-metadata -i 0 -w 0 -j ~/joystream/metadata.json --password=xxxxxxxx -k /root/keys/storage-role-key.json
```

### Checking opening

```
 yarn joystream-cli working-groups:openings
 yarn joystream-cli working-groups:opening --id 2
 yarn joystream-cli working-groups:application
 yarn joystream-cli working-groups:application 2
```

### Setup Storage default

```
 yarn storage-node leader:update-voucher-limits -s 2000000000000 -o 20000 -k /root/keys/storage-role-key.json
 yarn storage-node leader:update-voucher-limits -s 2000000000000 -o 20000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:set-bucket-limits -i 0 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:set-bucket-limits -i 0 -o 20000 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Hiring worker 1

```
 yarn joystream-cli working-groups:fillOpening --openingId 4 --applicationIds 2
 yarn joystream-cli working-groups:overview
 yarn joystream-cli working-groups:application
 yarn joystream-cli working-groups:application --help
 yarn storage-node leader:create-bucket -i 1 -n 20000 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-bucket-status -i 1 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Activating worker 0

```
 yarn storage-node leader:update-bucket-status -i 0 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Hiring worker 2

```
 yarn joystream-cli working-groups:fillOpening --openingId 4 --applicationIds 1
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
 yarn joystream-cli working-groups:fillOpening --openingId 6 --applicationIds 4
 yarn joystream-cli working-groups:overview -g=storageProviders
 yarn storage-node leader:create-bucket -i 2 -n 20000 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-bucket-status -i 2 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
```

## Nov-27-2022

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | 0x2bc |
| 2 | maxlevush |
| 3 | sieemma |

**Performed tasks:**

- Created openings for Storage Workers
- Hired worker 3 deputy lead
- Created opening for ES worker
- Onboarding workers

**Executed commands:**

### Hiring worker 3

```
 yarn joystream-cli working-groups:fillOpening --openingId 2 --applicationIds 11
 yarn joystream-cli working-groups:overview -g=storageProviders
 yarn storage-node leader:create-bucket -i 3 -n 20000 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn storage-node leader:update-bucket-status -i 3 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
 yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_ES_Worker.json
```

## Nov-28-2022

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | 0x2bc |
| 2 | maxlevush |
| 3 | sieemma |

**Performed tasks:**

- Onboarding workers
- Updated rewards
- Updated documentation

**Executed commands:**

### Activating worker 1&2

```jsx
yarn storage-node leader:update-bucket-status -i 1 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:update-bucket-status -i 2 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Update rewards

```jsx
yarn joystream-cli working-groups:updateWorkerReward 1 23116040 --group=storageProviders
yarn joystream-cli working-groups:updateWorkerReward 2 23116040 --group=storageProviders
yarn joystream-cli working-groups:updateWorkerReward 3 46232090 --group=storageProviders
```

## Nov-29-2022

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | 0x2bc |
| 2 | maxlevush |
| 3 | sieemma |
| 4 | **Craci_BwareLabs** |

**Performed tasks:**

- Hired worker 4
- Onboarding workers
- Updated documentation

**Executed commands:**

### Updated bag policy (Make sure policy not exceed active nodes)

```jsx
yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 3 -k /root/keys/storage-role-key.json -p xxxxxx
```

### Hire worker 4

```jsx
yarn joystream-cli working-groups:fillOpening --openingId 5 --applicationIds 12
yarn joystream-cli working-groups:updateWorkerReward 4 23116040  --group=storageProviders
yarn storage-node leader:create-bucket -i 4 -n 20000 -s 2000000000000 -k /root/keys/storage-role-key.json -p xxxxxx
yarn storage-node leader:update-bucket-status -i 4 -s off -k /root/keys/storage-role-key.json -p xxxxx
```

### Recreated the opening

```jsx
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
yarn joystream-cli working-groups:cancelOpening 8
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
```

### Re-invite worker 3 (server migration)

```jsx
yarn storage-node leader:remove-operator -i 3 -k /root/keys/storage-role-key.json -p xxxxxx
yarn storage-node leader:invite-operator -i 3  -w 3 -k /root/keys/storage-role-key.json -p xxxxx
```

### Activate worker 3

```jsx
yarn storage-node leader:update-bucket-status -i 3 -s on -k /root/keys/storage-role-key.json -p xxxxx
```

## Nov-30-2022

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | 0x2bc |
| 2 | maxlevush |
| 3 | sieemma |
| 4 | **Craci_BwareLabs** |

**Performed tasks:**

- Onboarding workers
- Updated documentation

**Executed commands:**

# Mainnet  **work**

[Lead docs](https://github.com/yasiryagi/community-repo/tree/master/working-groups/storage-group/leader) 

[Team detail](https://docs.google.com/spreadsheets/d/1Zu_RIJ1rAChJx637u7Ua7A8lVrT6TjigXdTWIRxxRl8/edit#gid=0)

## Jan-06-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |

**Performed tasks:**

- Initial storage setup.
- Setup Lead server.
- Agreed with council on network parameters.
- Created opening

**Executed commands:**

### Set env

```
yarn joystream-cli api:setQueryNodeEndpoint  yarn joystream-cli api:setQueryNodeEndpoint  
yarn joystream-cli account:import  --backupFilePath  /root/keys/storage-role-key.json  
yarn joystream-cli working-groups:setDefaultGroup -g storageProviders  
yarn joystream-cli working-groups:overview -g=storageProviders
```

### Creating opening

```
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json 
yarn joystream-cli working-groups:cancelOpening 1 
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
yarn joystream-cli working-groups:cancelOpening 2 
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
```

### Setup Storage default

```
yarn storage-node leader:update-voucher-limits -s 10000000000000 -o 20000 -k /root/keys/storage-role-key.json -p xxxxxxxx 
yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 5 -k /root/keys/storage-role-key.json -p xxxxxxxx 
yarn storage-node leader:update-bag-limit -l 5 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Creating bucket for worker 0 (lead)

```
yarn storage-node leader:create-bucket -i 0 -n 20000 -s 10000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxx  
yarn storage-node leader:update-bucket-status -i 0 -s off -k /root/keys/storage-role-key.json -p xxxxxxxx
```

## Jan-07-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |

**Performed tasks:**

- Setup Lead server.
- Update deployment documentation
- Hired works
- Created workers buckets
- Created ES worker opening

**Executed commands:**

### Set lead server

```
 yarn run storage-node operator:accept-invitation -i 0 -w 0 -t 5CPhA9RkPnykLxGy1JVy1Y4x9YPSYq9iq48NAMzoKXX9mLG8 --password=xxxxxxxx -k /root/keys/storage-role-key.json 
yarn run storage-node operator:set-metadata -i 0 -w 0 -j ~/joystream/metadata.json      --password=xxxxxxxxxx -k /root/keys/storage-role-key.json
```

### Accept application

```
yarn joystream-cli working-groups:fillOpening --openingId 3 --applicationIds={3,4,5,7}
```

### Create workers buckets

```

yarn storage-node leader:create-bucket -i 1 -n 20000 -s 8000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:update-bucket-status -i 1 -s off -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:create-bucket -i 2 -n 20000 -s 10000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:update-bucket-status -i 2 -s off -k /root/keys/storage-role-key.json -p xxxxxxxxxx 
yarn storage-node leader:create-bucket -i 3 -n 20000 -s 10000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:update-bucket-status -i 3 -s off -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:create-bucket -i 4 -n 20000 -s 10000000000000 -k /root/keys/storage-role-key.json -p xxxxxxxxxx
yarn storage-node leader:update-bucket-status -i 4 -s off -k /root/keys/storage-role-key.json -p xxxxxxxxxx
```

### Enable Bucket 0 (lead)

```
yarn storage-node leader:update-bucket-status -i 0 -s on -k /root/keys/storage-role-key.json -p xxxxxxxxxx
```

### Create ES worker opening

```
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_ES_Worker.json
```

## Jan-08-202

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |

**Performed tasks:**

- Update documentation
- Onboarding workers

**Executed commands:**

### Create opening

```
yarn joystream-cli working-groups:createOpening -i /root/community-repo/working-groups/storage-group/leader/opening/Strorage_WG_Worker.json
```

## Jan-09-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Update documentation
- Onboarding workers
- Hired ES worker
- Plan and Report template

**Executed commands:**

### Activate worker 2 bucket

```
yarn storage-node leader:update-bucket-status -i  2 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Hired ES worker

```
yarn joystream-cli working-groups:fillOpening --openingId 4 --applicationIds=1
```

### Update replication

```
yarn storage-node leader:update-bag-limit -l 4 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

## Jan-10-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Update documentation
- Onboarding workers

**Executed commands:**

### Activate worker 2 bucket

```
yarn storage-node leader:update-bucket-status -i  1 -s on -k /root/keys/storage-role-key.json -p xxxxxxxx
```

### Change replication

```jsx
yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 4 -k /root/keys/storage-role-key.json -p xxxxxxxx
yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 3 -k /root/keys/storage-role-key.json -p xxxxxxxx 
yarn storage-node leader:update-bag-limit -l 3 -k /root/keys/storage-role-key.json -p xxxxxxxx
```

## Jan-11-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Onboarding workers
- Work on a monitoring and alerting setup

### Activate worker 3 bucket

```
 yarn storage-node leader:update-bucket-status -i 3 -s on -k /root/keys/storage-role-key.json -p xxxxx
```

## Jan-12-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Onboarding workers
- Work on a monitoring and alerting setup

## Jan-13-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Onboarding workers
- Work on a monitoring and alerting setup

## Jan-14-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Onboarding workers
- Work on a monitoring and alerting setup

## Jan-15-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Onboarding workers
- Work on a monitoring and alerting setup

### Jan-16-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

**Performed tasks:**

- Worked on capacity plan
- Work on a monitoring and alerting setup

### Jan-17-2023

Hired workers:

| Worker ID | Joystream Name |
| --- | --- |
| 0 | yyagi (Lead) |
| 1 | Maxlevush | COIN SIDE#6419 |
| 2 | Craci | [bwarelabs.com#0141](http://bwarelabs.com/#0141) |
| 3 | GokselAtasert08#9188 |
| 4 | 0x2bc |
| 5 | joystreamstats |

- **Performed tasks:**