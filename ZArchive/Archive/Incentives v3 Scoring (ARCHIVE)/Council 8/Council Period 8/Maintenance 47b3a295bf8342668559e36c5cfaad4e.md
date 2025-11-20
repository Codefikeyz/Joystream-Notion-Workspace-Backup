# Maintenance

Group: Storage
Score Status: Completed
Score: 1
Attributes: Grade
Reports Gathered: No
Grade Name: MAINTENANCE_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#maintenance_score
Parent Score: Storage Score (Storage%20Score%20252ea415198d48d78beeb34b391b9f6f.md)
Score Type: Subscore
Spot Check Completed: No

Spotcheck made at the end of the period, using [**grading tools](../../../Tools%20and%20Resources%20(ARCHIVE)%208969641b5b284d1c85c658106a79792d.md):**

```markdown
yarn joystream-cli incentives:storageMaintenance -s 748800,849600 -m 4

# Which returns:

dynamic_configuration_score = 1
Out of 624 bags, 7 are in fewer than 4 buckets
## Removed from the count - testing bags
existing_bag_configuration_score = 1
{
  dynamic_configuration_score: 1,
  existing_bag_configuration_score: 0,
  excess_capacity_objects_false: 19960,
  excess_capacity_size_false: 998,
  excess_capacity_objects_true: 5714,
  excess_capacity_size_true: 541
}

excess_capacity_objects_score = [max((19960-75)/75,1)) + max((5714-200)/200,1))]/2 = 1
excess_capacity_size_score = [max((998-10)/20,1)) + max((541-30)/20,1))]/2 = 1

MAINTENANCE_SCORE = (1+1+1+1)/4 = 0.75
```