# Uploads

Group: Storage
JSG Grading Status: Not Completed
Attributes: Grade
Reports Gathered: No
Grade Name: UPLOAD_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#upload_score
Parent Score: Storage Score (Storage%20Score%20dfc2866b23ed424a931819abc445d27c.md)
Score Type: Subscore
Spot Check Completed: No

Using the [grading tools](../../../Tools%20and%20Resources%20(ARCHIVE)%208969641b5b284d1c85c658106a79792d.md):

```markdown
yarn joystream-cli incentives:storageUploads -s 1652568672000 -e 1653174438003

# Where the values are the timestamps of the first and last block

total_uploads = 69
successful_uploads = 68
failed_uploads = 1
Which gives:
UPLOAD_SCORE = 0.927536231884058
```