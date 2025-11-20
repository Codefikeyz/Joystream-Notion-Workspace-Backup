# Tools and Resources (ARCHIVE)

In the attempt to make the grading process more transparent, some tools we use will over time be added here.

- Dashboards: [https://joystream.gitbook.io/testnet-workspace/testnet/dashboards](https://joystream.gitbook.io/testnet-workspace/testnet/dashboards)
- Grading: [https://github.com/bwhm/joystream/tree/incentives-tools](https://github.com/bwhm/joystream/tree/incentives-tools)

```
Tools to compute and verify rewards and grading.

USAGE
  $ joystream-cli incentives:COMMAND

COMMANDS
  incentives:councilSpending        Gets stats
  incentives:distributionStats      Gets storage replication statistics
  incentives:getBountyInfo          Gets stats
  incentives:getContentStats        Gets stats
  incentives:getContentStatsOld     Gets stats
  incentives:getForumStats          Gets stats
  incentives:getForumStatsOld       Gets stats
  incentives:getOpenings            Gets worker/lead statistics one or more groups
  incentives:getOpportunitiesScore  Gets stats
  incentives:getWorkersStats        Gets worker/lead statistics one or more groups
  incentives:storageMaintenance     Gets storage replication statistics
  incentives:storageMaintenanceOld  Gets storage replication statistics
  incentives:storageUploads         Gets storage replication statistics
  incentives:validatorRewards       Gets stats
```

tracker: https://github.com/Joystream/founding-members/issues/108

# Preparation

If you cloned the [joystream repo](https://github.com/Joystream/joystream) before:

```
cd joystream/cli
git remote add bwhm https://github.com/bwhm/joystream
git fetch bwhm
git checkout bwhm/incentives-tools --track
```

otherwise: `git clone https://github.com/bwhm/joystream -b incentives-tools grading --depth 3 --single-branch ; cd grading/cli`

# Usage

Find term boundaries here [](Incentives%20v3%20Scoring%20(ARCHIVE)%20b9ea7c6923e74539941477d1a2e083a6.md) 

```jsx
start=1152000
end=1252800

./bin/run incentives:councilSpending $start $end
```

example: [https://joystreamstats.live/static/grading12/councilSpending.txt](https://joystreamstats.live/static/grading12/councilSpending.txt)