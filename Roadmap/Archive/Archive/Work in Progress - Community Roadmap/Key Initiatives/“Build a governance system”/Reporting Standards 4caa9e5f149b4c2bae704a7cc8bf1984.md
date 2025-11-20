# Reporting Standards

Tags: governance tools, policies, reports, standards, working groups
Action Status: likely to be actioned
Writing Status: Draft, Heavy research required
Proposal Status: Unproposed
Discussion Status: Undiscussed

[https://github.com/Joystream/community-repo/issues/499](https://github.com/Joystream/community-repo/issues/499)

## **Problem & Goal**

Currently, on Joystream, a variety of reports are created each week, this includes (which will expand when more WGs are added):

- Council Tokenomics reports folder (45 files, spread across 7 folders)
- Council Minutes reports folder (52 files, spread across 7 folders)
- Storage WG reports folder (22 files in 1 folder)
- Curator WG reports folder (24 files in 1 folder)
- Operations WG reports folder (11 files in 1 folder)

These reports often give a deep insight into the performance of each working group that goes beyond what simple lead and worker payments can provide. However, they are very difficult to access and parse due to the structure in which they currently exist.

Due to the number of report files and the combined number of folders a user will have to navigate through a total of `22 folders` which contain `154 files`. This is obviously a very poor user experience.

We need to come up with a better system to improve this.

## **Requirements**

- Creating some form of more centralized/standard method of reports, which can far more easily be parsed by users and should move on from the current system of files and folders to improve readability.

## **Current Problems**

- many lead reports are done through individual files, which makes it difficult to collate/compare information
- each report has quite different formats depending on who the lead is
- all of the information is separated by the WG that creates it
- OKRs are not included in these reports
- the council leaderboard ([https://docs.google.com/spreadsheets/d/1l_aFoN2GxFpxi7pZS3rUh9wCsVHUi8um4YYiNRWMBW8/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1l_aFoN2GxFpxi7pZS3rUh9wCsVHUi8um4YYiNRWMBW8/edit?usp=sharing)) has slowly turned into a very giant spreadsheet, although it does incorporate charts, the Google Sheets website has issues with these that often require repeated manual intervention to fix.
- the number of cells in the council leaderboard is so extensive that is becoming tedious to manually update by using council minutes and tokenomic reports

## **Notes**

- The new storage system releasing in `giza` will allow working groups to store their own data, I am not entirely clear on whether it is feasible to store markdown or text files on this system

## **Potential improvements**

- Combining all reports from all working groups and the council's reports (minutes and tokenomics) into one central system, maybe a JSON file or some form of database.
- Allowing search of specific leads/workers across different working groups and being able to understand their quality and identifying possible malicious users