# Limitations of Forum (Testnet)

The runtime has some limitations when it comes to the forum, they are defined here: [https://github.com/Joystream/joystream/blob/master/runtime/src/lib.rs#L734](https://github.com/Joystream/joystream/blob/master/runtime/src/lib.rs#L734)

L1dev [put together](https://discord.com/channels/811216481340751934/956881993449242654/957373229150920735) a nice list:

- You can have max 6 levels of categories
- Each category can have 20 subcategories
- Each category can have 20 threads
- Each thread can have 20 posts
- Each category can have 20 moderators
- There can ban 20 top-level categories in total
- There can be 20 possible answers in polls (not sure about that one)
- PostLifeTime: 3600 blocks (Maximum number of blocks before a post can be erased by anyone)