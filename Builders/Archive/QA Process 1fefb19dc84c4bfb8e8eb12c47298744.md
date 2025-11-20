# QA Process

Testers are encouraged to use this process in their day to day activities! 

1️⃣  Lead assigns *community-dev* and *qa-task* issues to individual workers. ⚠️ UAT on staging cannot be done by PR authors.
2️⃣  Test assigned issues, all the scenarios and acceptance criteria. described in the issue on [**dao-git-staging-joystream.vercel.app**](https://dao-git-staging-joystream.vercel.app)
3️⃣  Depending on result move the issue to the respective pipeline, tagging the issue with labels:

✅  "tested-ready-for-prod" for success

⏳ Additionally, QA must set a label indicating time efforts to test this issue: 

![Screenshot_2022-04-27_at_10.47.37.png](QA%20Process/Screenshot_2022-04-27_at_10.47.37.png)

🚫  "tested-failed" for failed scenarios

⚠️   Add detailed evidences of both successful or failed outcomes to the comments of the issue, such as 📸  screenshots or 🎥  video link ⚠️

4️⃣  QA pings the Lead when testing is finished, Lead moves the task to “Ready for Prod”

### Open questions

What to do when QA thinks that acceptance criteria are unclear. Leave a comment, tag someone, ticket is left in Ready for QA?