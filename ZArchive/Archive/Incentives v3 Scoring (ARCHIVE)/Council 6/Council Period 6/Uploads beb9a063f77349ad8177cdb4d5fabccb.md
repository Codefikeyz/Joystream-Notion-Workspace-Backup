# Uploads

Group: Storage
Score Status: Ready for review
Score: 0.714
Attributes: Grade
Reports Gathered: No
Grade Name: UPLOAD_SCORE
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/storage-providers-score#upload_score
Parent Score: Storage Score (Storage%20Score%2081b017cd1afa4f8b9ceebde3f66d7d6a.md)
Score Type: Subscore
Spot Check Completed: No

With a QN synced to 663066

```markdown
query Failed_Uploads {
  storageDataObjects (limit:1000000, where:{createdAt_gte:"Sat Apr 30 2022 22:17:18 GMT+0000",createdAt_lte:"Sat May 07 2022 22:30:12 GMT+0000"}) {
    id
    isAccepted
    size
    ipfsHash
    createdAt
    updatedAt
    storageBag {
      id
      storageBuckets {
        id
      }
    }
  }
}
```

Only `isAccepted` is strictly needed, but the others includes context should the Lead include reasons to avoid in their reports.

```markdown
UPLOAD_SCORE = (successful_uploads/total_uploads - 0.80)/0.20
= (181/(181+11) - 0.8)/0.2) = 0.714
```