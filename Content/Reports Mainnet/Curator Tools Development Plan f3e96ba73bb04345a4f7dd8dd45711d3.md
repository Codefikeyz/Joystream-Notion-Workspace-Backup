# Curator Tools Development Plan

# Prerequisites

For a long time, starting with testnets, curators have been keeping records of verified videos in a Google Sheets table. Unfortunately, the disadvantages of this system are obvious: this table no longer holds one term and often you have to create a new table, and it is also slow. The list of new videos is sometimes added slowly, the node does not produce records for about 20 thousand videos, and sometimes you have to upload the data in parts. The main problem is that the videos themselves in Joystream are not marked as verified on-chain. At the request of a group of curators, Curator Tools were created. A group of curators hope this will alleviate some of the problems associated with inconvenience. The most important problem has not been solved - all accounting is kept OUTSIDE the Joystream blockchain and does not belong to the community. But the Tools have been created and have a minimal set of functionality, and there are a number of problems that require attention and correction.

# Near-term development plan

First priority:

1. Adding statistics on video curators, like on administrator page + indicating how many toxic videos there were, duplicates, distribution by category;
2. Now, when checking a video and moving to the next video, the curator must first press the “Submit” button, only then Next; when simply switching to the next video, the entered data is not saved. You need to remove the “Submit” button and save all changes when moving to the next video;

Second priority:

1. The Curator Tools database does not automatically synchronize with the blockchain. Instead, when you select a time range, if there are differences, the refresh button becomes available. It is required that the curator's tools update and synchronize every day after midnight for the previous day, log the synchronization and display it in the administrative panel: for example, in the case of complete synchronization of one day in the calendar, it is marked in green or successful synchronization is displayed in text;
2. Assigning checks to curators is done manually and has some problems. A maximum of 100 videos can be placed on a page in the administrative panel and there is no way to assign all videos that meet the filters with one click if there are more than 100 of them and there is no accounting for the assignments. In addition to the basic option of assigning a list of videos to curators, it is required to create a schedule by day (from 00:00 of one day to 00:00 of the next day) with the ability to pre-distribute future days for the curator. The video destination should determine that the video list will be automatically distributed according to the selected filters at the next sync after midnight. The schedule should be publicly available so that supervisors can plan their time;
3. The uploaded data must also contain information about the duration of the video, occupied space, and channel ID;
4. In the administrative panel, when selecting some filters, the list is not updated instantly, and the processing process is not visible. It is necessary to add a notification after selecting filters that the displayed list is irrelevant, color the list in a faded color or remove it until the data is loaded;
5. In the administrative panel, when selecting a date range, the time is set based on the actual time. Requires 00:00 to be selected by default as sampling is done in multiples of days (99.9% of cases);
6. Add the ability to filter by channel ID, by video ID, by channel name and by video title (add a search for videos containing the specified text). Add a link to Gleev.;
7. Add a Comment to the duplicate field to the verification page, available when you select “Yes” in the Duplicate field.

# Mid-term development plan

1. Creation of statistics containing a comparison of the number of videos by term, the number of non-YPP videos, volume, video duration, workload of curators by hour, distribution of videos by category, number of broken videos, number of illegal content, distribution by category;
2. Graphics output.

# Long term development plan

Add verification information to the Joystream blockchain.