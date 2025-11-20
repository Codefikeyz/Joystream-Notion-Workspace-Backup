# Maintenance

Group: Storage
Score Status: Ready for review
Score: 0.75
Attributes: Grade
Reports Gathered: No
Grade Name: MAINTENANCE_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#maintenance_score
Parent Score: Storage Score (Storage%20Score%2081b017cd1afa4f8b9ceebde3f66d7d6a.md)
Score Type: Subscore
Spot Check Completed: No

Dynamic config:

- `storage.dynamicBagCreationPolicies.at("hash(547200),channel)= 4`
- `storage.dynamicBagCreationPolicies.at("hash(648000),channel)= 4`

Existing config:

- With a query node synced up to block #663066:

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

Which shows 8 bags are only in 1 bucket.

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
acceptingBuckets [
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 840277,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13570,
        "excessCount": -6430,
        "excessSize": -1160
    },
    {
        "dataObjectsSizeLimit": 1500000,
        "dataObjectsSize": 840667,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13503,
        "excessCount": -6497,
        "excessSize": -659
    },
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 840331,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13521,
        "excessCount": -6479,
        "excessSize": -1160
    },
    {
        "dataObjectsSizeLimit": 1400000,
        "dataObjectsSize": 840597,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13641,
        "excessCount": -6359,
        "excessSize": -559
    },
    {
        "dataObjectsSizeLimit": 1400000,
        "dataObjectsSize": 840748,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13721,
        "excessCount": -6279,
        "excessSize": -559
    },
    {
        "dataObjectsSizeLimit": 2000000,
        "dataObjectsSize": 841616,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 13738,
        "excessCount": -6262,
        "excessSize": -1158
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
        "dataObjectsSize": 198,
        "dataObjectCountLimit": 20000,
        "dataObjectsCount": 22,
        "excessCount": -19978,
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