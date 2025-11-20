# Forum Moderation Guideline

**The purpose of the Forum Moderator Role**

Forum Moderator is responsible for the facilitation, review, and guidance of a discussion or a debate and its related interactions. Moderators use a standard or guideline to ensure that all the content shared during a discussion or debate is appropriate and adheres to the Forum Moderation Rule rules.

Moderator has to be ensure that he/she covers these action points:

- Discussions Facilitation;
- Thematic Control;
- Content Relevance;
- Orderly Conduct.

**Tools are required:**

- Console Emulator - Terminal (MacOS) or Cmder (Windows)
- Markdown Editor - Dillinger (online markdown editor)

**How to apply for the role:**

To apply for the position of Forum Moderator is quiet easy. You should find the [opening](https://dao.joystream.org/#/working-groups/forum), fill the survey and send an application. Make sure if opening is still relevant. It’s better to ask Forum Lead.

**Useful links:**

1. [**About Forum (in Handbook)**](https://joystream.gitbook.io/testnet-workspace/system/forum)
2. [**Forum Moderation Rules**](Moderation%20Rules%2012b336d78b0249bfbcf8c290a5872d45.md)
3. [How-to Setup Joystream CLI](How%20to%20Set-up%20Joystream%20CLI%20a773a8b8f6b749859e4b4d910cb142cf.md)
4. [**Joystream CLI Commands**](https://github.com/Joystream/joystream/tree/master/cli#joystream-cli-accountimport)
5. [**Joystream Pioneer Forum**](https://pioneerapp.xyz/#/forum)

**Category Structure** 

[List of Categories](../Mainnet%20Plans,%20Reports%20and%20Updates/List%20of%20Categories%20103deb8223c042fe96583587531adaeb.md)

**Forum Moderation CLI Commands accessible by Forum Lead and Workers**

- Move thread

```jsx
joystream-cli forum:moveThread -c categoryID -t threadID -n newcategoryID 

e.g. joystream-cli forum:moveThread -c 100  -t 200  -n 300
```

Video Tutorial: [How to Move Threads via CLI](https://gleev.xyz/video/281)

- How to “sticky” threads

```jsx
joystream-cli forum:setStickiedThreads --categoryId categoryID --threadId threadID

e.g. joystream-cli forum:setStickiedThreads --categoryId 25 --threadId 30
```

- Moderate thread (Delete thread)

```jsx
joystream-cli forum:moderateThread -c categoryID -t threadID -r "Rationale"

e.g. joystream-cli forum:moderateThread -c 100  -t 200  -r "duplicated thread"
```

Video Tutorial: [How to Delete Threads via CLI](https://gleev.xyz/video/282)

**Forum Moderation CLI Commands accessible by Forum Lead only**

- Create category

```jsx
joystream-cli forum:createCategory -t "Title" -d "Description"
```

- Delete category

```jsx
joystream-cli forum:deleteCategory -c categoryID

e.g. joystream-cli forum:deleteCategory -c 10
```

**Forum Moderation Extrinsics Commands accessible by Forum Lead and Workers**

- Move thread
    1. Visit: [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/extrinsics](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/extrinsics)
    2. Choose your forum lead/moderator root account on ‘using the selected account’
        
        ![J.png](Forum%20Moderation%20Guideline/J.png)
        
    3. On ‘submit the folllowing extrinsics’ choose “forum”. Then, choose ‘moveThreadToCategory…’
        
        ![K.png](Forum%20Moderation%20Guideline/K.png)
        
    4. On ‘categoryID’ type existing category #, on ‘threadID’ type thread #, on ‘newCategoryId’ type intended new category #
        
        ![L.png](Forum%20Moderation%20Guideline/L.png)
        
    5. Click ‘Submit Transaction’ and sign wallet
        
        ![M.png](Forum%20Moderation%20Guideline/M.png)
        
    

- Moderate thread (Delete thread)
    1. Visit: [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/extrinsics](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/extrinsics)
    2. Choose your forum lead/moderator root account on ‘using the selected account’
        
        ![J.png](Forum%20Moderation%20Guideline/J.png)
        
    3. On ‘submit the folllowing extrinsics’ choose “forum”. Then, choose ‘moderateThread…’
        
        ![N.png](Forum%20Moderation%20Guideline/N.png)
        
    4. Type category ID # and thread ID #
        
        ![O.png](Forum%20Moderation%20Guideline/O.png)
        
    5. Type the reason for moderating the thread
        
        ![P.png](Forum%20Moderation%20Guideline/P.png)
        
    6. Click ‘Submit Transaction’ and sign wallet
        
        ![R.png](Forum%20Moderation%20Guideline/R.png)