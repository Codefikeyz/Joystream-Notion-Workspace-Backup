# Maintenance

Group: Storage
JSG Grading Status: Completed
Score: 1
Attributes: Grade
Grade Name: MAINTENANCE_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#maintenance_score
Parent Score: Storage Score (Storage%20Score%20425b22fc33c342e9af5fc54c7e4691f1.md)
Score Type: Subscore
Spot Check Completed: No

```markdown
yarn joystream-cli incentives:storageMaintenance -s=849600,950400 -m 4 -i=2333,2334,2335,2336,2337,2338,2339
# returns

dynamic_configuration_score = 1
Out of 628 bags, 0 are in fewer than 4 buckets
existing_bag_configuration_score = 1
{
  dynamic_configuration_score: 1,
  existing_bag_configuration_score: 1,
  excess_capacity_objects_false: 19960,
  excess_capacity_size_false: 998,
  excess_capacity_objects_true: 5650,
  excess_capacity_size_true: 537
}

dynamic_configuration_score = Zigma[max(dynamic_configuration_i-3,1)]/i
= 1
existing_bag_configuration_score = Zigma[max(existing_bag_configuration_i-3,1)]/i
= 1
excess_capacity_objects_false_score = Zigma[max((excess_capacity_objects_i-75)/75,1)]/i
= 1
excess_capacity_size_false_score = Zigma[max((excess_capacity_size_i-10)/20,1)]/i
= 1
excess_capacity_objects_true_score = Zigma[max((excess_capacity_objects_i-200)/200,1)]/i
= 1
excess_capacity_size_true_score = Zigma[max((excess_capacity_size_i-30)/20,1)]/i
= 1

  # finally
  MAINTENANCE_SCORE = 0.25*(dynamic_configuration_score + existing_bag_configuration_score + excess_capacity_objects_score + excess_capacity_size_score)
= 1
```