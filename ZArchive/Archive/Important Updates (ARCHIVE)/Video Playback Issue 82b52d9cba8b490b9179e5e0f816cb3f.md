# Video Playback Issue

Areas Impacted: Atlas, Video Playback
Current Status: Ongoing
Severity: Low, PSA
Time of incident: May 24, 2022 7:00 PM (GMT+1)
Type: Infrastructure
Created at: May 25, 2022 8:33 AM
Last Updated: May 25, 2022 8:47 AM

<aside>
💡 If you happen to come across certain videos that you cannot get to play, or you notice peculiar or notable information while loading content, please share it in the #bug-reports channel on Discord.

</aside>

It appears some users have had issues playing back videos recently. There are a wide number of possible reasons but based on a quick investigation some of the reasons may be attributable to the following:

- There have been more users joining the community, which has in turn very likely created more load on the infrastructure operated by JSG (such as the Query Node and Orion node).
    - In particular, the Orion node seems to be experiencing high latency.
- There has also been more load on the Distributor Nodes (which host video files for end-users/viewers to access)
    - Some distributor nodes seemed to be suffering from poor speeds or extremely high latency (2 events were recorded in which 2 distributor nodes failed to respond within 20,000 seconds)
- On top of the root issues causing playback problems, there are currently poor measurement tools available which means it is tedious and time consuming to check the status of JSG and/or community infrastructure and to objectively measure the experience of users trying to play videos on Atlas. This is also actively being looked into.

Further investigation is ongoing and we will try to identify the root causes of this as soon as possible. No ETA is currently available for a fix as this is an issue that is impacted by multiple layers of infrastructure and tooling, however it is obviously a goal to have a video platform that is highly reliable.