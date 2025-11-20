# How to calculate DAO workers salary

Resource links:

[https://pioneer.joystreamstats.live/#/council/past-councils](https://pioneer.joystreamstats.live/#/council/past-councils)

[](https://query.joystream.org/graphql)[https://www.convertcsv.com/json-to-csv.htm](https://www.convertcsv.com/json-to-csv.htm)

[https://www.notion.so/joystream/Working-Group-Database-e8a1059e3fa44efeb2e5c3184e633d70](https://www.notion.so/Working-Group-Database-e8a1059e3fa44efeb2e5c3184e633d70?pvs=21)

[https://www.notion.so/joystream/WG-s-title-96639fc771034dcf81d0cf3acc07ba7a](Maria/WG%E2%80%99s%20title%2096639fc771034dcf81d0cf3acc07ba7a.md)

[https://docs.google.com/spreadsheets/d/1u0s8sN7RnIgyA9AbF6c2wq08PRtZK9iuDkov-J3t1Xg/edit#gid=974516064](https://docs.google.com/spreadsheets/d/1u0s8sN7RnIgyA9AbF6c2wq08PRtZK9iuDkov-J3t1Xg/edit#gid=974516064)

[https://query.joystream.org/graphql](https://query.joystream.org/graphql)

query {
rewardPaidEvents
(
limit:1000000,
where:{inBlock_gte:2937613,inBlock_lte:3153614, group: {
name_eq:"contentWorkingGroup"
}}) {
amount
worker {
membership {
handle
}
}
}

}

Graphic Tutorial: [https://www.notion.so/joystream/Guide-how-to-track-salary-history-20a260051ae14036804c621ba8a77507](Maria/Guide%20how%20to%20track%20salary%20history%2020a260051ae14036804c621ba8a77507.md)

[WIP Joystream’s members](How%20to%20calculate%20DAO%20workers%20salary/WIP%20Joystream%E2%80%99s%20members%202a00397eed9848e49899096ce8523c04.csv)