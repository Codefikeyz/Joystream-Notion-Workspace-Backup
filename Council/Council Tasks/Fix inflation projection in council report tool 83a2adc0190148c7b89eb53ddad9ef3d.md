# Fix inflation projection in council report tool

Public Notion URL: https://joystream.notion.site/83a2adc0190148c7b89eb53ddad9ef3d
Tags: builders WG, council
Created time: March 15, 2024 12:16 PM
Work Status: Done
Governance Status: Not started
Archive Status: No
Days passed since task created: 614
Last edited time: June 9, 2024 7:34 PM

Problem: 
The inflation projection is incorrect and appears to just be a sum of all council terms since mainnet launch—it also doesn’t calculate inflation from the current issuance.

- Full problem (written by tomato)
    
    so there are 3 issues:
    
    - example report: [https://pioneerapp.xyz/#/forum/thread/855](https://pioneerapp.xyz/#/forum/thread/855)
    - `"Projected inflation this year: 4.9%"` - the problem is that this is just the "total inflation". Projected inflation would take like the current council's inflation % and multiply it by 12 (assuming a 1 month council period--but we're actually doing 28 day council periods haha).
    - The number is vastly wrong at this point, that was a report from a 2 week council term, which means you would times the "planned inflation for this term" of `0.184%` by 26 (because 2 weeks terms), so the "projected inflation" *should* be `4.784%`-but the "projected inflation" shown is `4.9%`.
    - 2nd example report: [https://pioneerapp.xyz/#/forum/thread/873](https://pioneerapp.xyz/#/forum/thread/873) the term's projected inflation was `5.952%` but should actually be `6.448%`
    - I really don't think "projected inflation" should be based on just the current terms inflation, because it will increase/decrease slightly, it should use like the last quarter or something--this will be annoying to do now because we have a mix of 2 week and 28 day council terms.
    - Then the second problem is that the table in the report shows `total` down the bottom--in the first report you will see that it is `4.9%`. `This` is what is being used for "projected inflation" which is totally wrong. It is basically summing the inflation from 29 council terms which is `58 weeks` and using it to show inflation--this is also totally wrong. We should never show inflation for anything longer than a year.
    - If we adjust the table to only show `26 terms` (by removing the first 3 council terms) then it is only `4.47%` for the past calendar year. That's a difference of like ~0.5% which is substantial--it's like a `10% increase` from what inflation actually is
    
    The consequences of that are two-fold:
    
    - The council/DAO/community are making decisions about inflation and saying `"hey we can/can't afford this or that"` and using the inflation numbers to make decisions--and if the data is incorrect then it is basically blind decision making or at last decision making based on bad data
    - Investors etc may look at our reports and either say "omg the inflation is too high" `or` the worse option is that they see how inflation is being calculated and think we don't know what we're doing or something like that
    - I `think` the inflation amounts on the `Weekly roundup` are correct, but I'm not sure: [https://blog.joystream.org/weekly-roundup-31/](https://blog.joystream.org/weekly-roundup-31/)
    - oh yeah, I also forgot that the inflation of each term is also incorrect--the %s are based off inflation from 1 billion initial issuance. I don't have a finance background so I don't know if the inflation each term should be calculated from what the current issuance is or if inflation for the year should be based off whatever the issuance was 12 months ago

April 9, 2024 

- Communicated this with the BWGL
- Was asked to make a GH issue to state the desired behavior/environemnt
- Gathered more insights from other people (Tomato has written them above, thank you)
- As per 0x2bc, he emphasized the need to change the value being used for the ***total token current supply*** since it seemed to be fixed at 1B Joy initial supply.