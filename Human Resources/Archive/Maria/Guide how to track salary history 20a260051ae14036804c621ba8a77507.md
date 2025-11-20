# Guide how to track salary history

1. In order to obtain salary information, you need to prepare the following data points: the start and end of the term and the [WG’s title](WG%E2%80%99s%20title%2096639fc771034dcf81d0cf3acc07ba7a.md).
2. You can find the start and end blocks here [https://pioneerapp.xyz/#/election/past-elections](https://pioneerapp.xyz/#/election/past-elections). An example:

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled.png)

Here we can check the start and the end of the term in blocks: 345601 and 561602. 

1. Enter the necessary data: the period in blocks and the title of the working party

<aside>
💡

query {
rewardPaidEvents
(
limit:1000000,
where:{inBlock_gte:**1857608**,inBlock_lte:**2073609**, group: {
name_eq:"operationsWorkingGroupAlpha"
}}) {
amount
worker {
membership {
handle
}
}
}

}# Write your query or mutation here

</aside>

Just open the link and insert the required values**:** 

[https://query.joystream.org/graphql](https://query.joystream.org/graphql)

Press the play button. After that in the right column, you will see the output of all data.

1. **Select and copy this data:**
(Attention! Strictly: not manually, but with your keyboard - ctrl (windows) or cmd (ios) + A (All), so that all lines are copied exactly!)
2. **And paste this data into the online converter:** 

<aside>
💡 [https://www.convertcsv.com/json-to-csv.htm](https://www.convertcsv.com/json-to-csv.htm)

</aside>

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled%201.png)

### Receive data in the **CSV** format

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled%202.png)

1. I work in google table https://docs.google.com/spreadsheets/d/1QjSh2Gsw2XlGQ3ObTBCcigwrr8DN6LDUSQfLFrKcW0M/edit#gid=1568333434 

I paste the data into the Google table, divide the text into columns

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled%203.png)

then copy the data and transfer it to another sheet. Then copy the names of all workers, insert the data in a separate column, and delete all the repetitions 

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled%204.png)

using the formula **SUMIF**

![Untitled](Guide%20how%20to%20track%20salary%20history/Untitled%205.png)

# result: ferdikesh_studio received 1.489 JOY for the 03th term.