# Maintena

Group: Storage
Score Status: Not Completed
Score: 0.75
Attributes: Grade
Reports Gathered: No
Grade Name: MAINTENANCE_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#maintenance_score
Parent Score: Storage Score (Storage%20Score%20bdef29f3ae2143378688c425c8a12f94.md)
Handover Weight: 1
Builder Weight: 4
Score Type: Subscore
Spot Check Completed: No
Content Weight: 2
Distributor Weight: 3
Forum Weight: 1
HR Weight: 4
Lead Opportunities Weight: 1
Marketer Weight: 0
Marketing Weight: 0
Plan Weight: 1
Property 1: 2
Property 2: 4
Scoring Weights: Council 7 (../../Council%207%207f116be5a8f54180abd97510bc5cfbc7.md)
Storage Weight: 3
Summary Weight link: 1

Dynamic config:

- `storage.dynamicBagCreationPolicies.at("hash(547200),channel)= 4`
- `storage.dynamicBagCreationPolicies.at("hash(648000),channel)= 4`

Existing config:

- With a query node synced up to block #748814:

```markdown
query storageReplication {
  storageBags (limit:1000000) {
    id
    createdAt
    storageBuckets {
      id
    }
  }
}
```

Which shows 7 bags are only in 1 bucket.

`excess_capacity`:

```markdown
query Storage_Maintanence {
  storageBuckets {
    id
    acceptingNewBags
    dataObjectsSizeLimit
    dataObjectCountLimit
    dataObjectsCount
    dataObjectsSize
    operatorStatus {
      ... on StorageBucketOperatorStatusActive {
        workerId
      }
    }
    operatorMetadata {
      nodeEndpoint
    }
  }
}
```

Script returns:

```markdown
	dynamic_configuration_score = Zigma[max(dynamic_configuration_i-3,1)]/i
= (1+1)/2

  existing_bag_configuration_score = Zigma[max(existing_bag_configuration_i-3,1)]/i
= 0

  excess_capacity_objects_false_score = Zigma[max((excess_capacity_objects_i-75)/75,1)]/i
= max((excess_capacity_objects_i-75)/75,1) = max((19978-75)/75,1) = 1

  excess_capacity_size_false_score = Zigma[max((excess_capacity_size_i-10)/20,1)]/i
= max((excess_capacity_size_i-10)/20,1) = max((997-10)/20,1) = 1

  excess_capacity_objects_true_score = Zigma[max((excess_capacity_objects_i-200)/200,1)]/i
= max((excess_capacity_objects_i-200)/200,1) = max((6262-200)/200,1) = 1

  excess_capacity_size_true_score = Zigma[max((excess_capacity_size_i-30)/20,1)]/i
= max((excess_capacity_size_i-30)/20,1) = max((559-30)/20,1 = 1

  # finally
  MAINTENANCE_SCORE = 0.25*(dynamic_configuration_score + existing_bag_configuration_score + excess_capacity_objects_score + excess_capacity_size_score)
= 0.25(1+0+1+1) = 0.75
```

```markdown
acceptingBuckets [
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 853778,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14178,
        "excessCount": -5822,
        "excessSize": -1146
    },
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 853926,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14166,
        "excessCount": -5834,
        "excessSize": -1146
    },
    {
        "dataObjectsSizeLimit": 1400000,
        "dataObjectsSize": 854369,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14232,
        "excessCount": -5768,
        "excessSize": -546
    },
    {
        "dataObjectsSizeLimit": 1400000,
        "dataObjectsSize": 854034,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14164,
        "excessCount": -5836,
        "excessSize": -546
    },
    {
        "dataObjectsSizeLimit": 1500000,
        "dataObjectsSize": 854157,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14202,
        "excessCount": -5798,
        "excessSize": -646
    },
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 854144,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 14218,
        "excessCount": -5782,
        "excessSize": -1146
    }
]
notAcceptingBuckets [
    {
        "dataObjectsSizeLimit": 1000000,
        "dataObjectsSize": 2580,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 12,
        "excessCount": -19988,
        "excessSize": -997
    },
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 265,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 40,
        "excessCount": -19960,
        "excessSize": -2000
    }
]
```

```markdown
	dynamic_configuration_score = Zigma[max(dynamic_configuration_i-3,1)]/i
= (1+1)/2

  existing_bag_configuration_score = Zigma[max(existing_bag_configuration_i-3,1)]/i
= 0

  excess_capacity_objects_false_score = Zigma[max((excess_capacity_objects_i-75)/75,1)]/i
= max((excess_capacity_objects_i-75)/75,1) = max((19960-75)/75,1) = 1

  excess_capacity_size_false_score = Zigma[max((excess_capacity_size_i-10)/20,1)]/i
= max((excess_capacity_size_i-10)/20,1) = max((997-10)/20,1) = 1

  excess_capacity_objects_true_score = Zigma[max((excess_capacity_objects_i-200)/200,1)]/i
= max((excess_capacity_objects_i-200)/200,1) = max((5768-200)/200,1) = 1

  excess_capacity_size_true_score = Zigma[max((excess_capacity_size_i-30)/20,1)]/i
= max((excess_capacity_size_i-30)/20,1) = max((546-30)/20,1 = 1

  # finally
  MAINTENANCE_SCORE = 0.25*(dynamic_configuration_score + existing_bag_configuration_score + excess_capacity_objects_score + excess_capacity_size_score)
= 0.25(1+0+1+1) = 0.75
```