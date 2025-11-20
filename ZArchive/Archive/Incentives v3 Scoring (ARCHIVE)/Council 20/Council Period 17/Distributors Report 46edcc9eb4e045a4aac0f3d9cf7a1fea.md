# Distributors Report

Group: Distributors
Attributes: Document, Forum Post, Grade, Group Specific Scores, Subscore
JSG Grading Status: Not Completed
Handbook Link: https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/distributors-score#report_score
Forum Report Source: https://dao.joystream.org/#/forum/category/15
Grade Name: REPORT_SCORE
Notion Link: Untitled (https://www.notion.so/e4ea2a85b1a84f88ba97c3580f685a09?pvs=21) 
Parent Score: Distributor Score (Distributor%20Score%20e60dcce3b9104ab19fd650450981fe80.md)
Spot Check Completed: No

I’m still quite curious as to what this is:

- “Aditionally [https://olympia.joystreamstats.live/storage](https://olympia.joystreamstats.live/storage) is constantly used. And [SP dashboard - Elastic (joystream.org)](https://atlas-services.joystream.org/kibana/app/dashboards#/view/cecb4ca0-792a-11ec-8b96-2be5a346ee21?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:now-30d,to:now))&_a=(description:'',filters:!(),fullScreenMode:!f,options:(hidePanelTitles:!f,useMargins:!t),query:(language:kuery,query:''),tags:!(),timeRestore:!t,title:'SP%20dashboard',viewMode:view)) is used to capture errors, response times etc.”

This is basically the same report as before, but new numbers. If correct, it’s very interesting that bucket `0:2` is consistently used so much more than the others…

## Questions and Comments

- (Still) no changes to setup, despite requested for a while now…
- Lots of missing, and not improved data.
- Of the 14 points:
    - 2 are not addressed (at all)
    - 4 are not addressed (properly)
    - 4 are presented poorly (generous)
    - `(14-2-(0.6*8))/14 = 0.5142857143`
        
        stricter with the partials this time
        
    

---

In addition to what is outlined in the [#working-group-period-plan](https://github.com/Joystream/handbook/blob/master/testnet/council-period-scoring/general-working-group-score.md#working-group-period-plan), the working group report must publish a separate report covering

- What was the setup of distribution family buckets, and buckets at the beginning and end of the term.
- What was the dynamic policy at the beginning and end of the term.
    - Not addressed
- How are bags distributed among the buckets in each bucket family.
    - Not addressed properly, as stated before
- What was the rationale behind the family bucket and bucket configuration, meaning
    - What geographical regions are the families meant to serve
    - Why was the specific dynamic bag policy chosen
    - How do you want to scale the system assuming a growth of 2x, 10x and 100x in terms of data objects and size
        - Not addressed properly, as stated before
- How much bandwidth did the individual nodes consume during the period.
- How is the bandwidth usage distributed, meaning
    - How did bandwidth usage look over a day (peak hours and slow hours)
    - How did bandwidth usage look over a week (peak days and slow days)
    - How did bandwidth usage look across regions (which regions consumes the most, if accessible)
    - How did bandwidth usage look across nodes, operators, buckets and families
- How are distributors supposed to set their `config.yaml` file and why.
- What is the current running costs for the system, and a breakdown of said costs.
- What, if anything, is the group doing the monitor the health of the system.
    - Not addressed properly, as stated before
- A list of all `storage` transactions (not `distributorWorkingGroup`) made by the lead, and the purpose behind them.