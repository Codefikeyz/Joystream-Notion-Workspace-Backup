# Mainnet Questions

**Working Group:** Forum WG
**Note:** These were the questions asked by council before mainnet launch and answered by lead

- **Write step by step guide how the work within your WG will be organized in the first term of the mainnet**
    - Organize group composition:
        1. Council will make a proposal for hiring a Lead
        2. Lead will be hired (1 person)
        3. Lead will hire first worker which will be Deputy Lead (1 person)
        4. Lead will hire Forum Curators (not yet sure how many) - If there will be influx of users from all over the world, we may hire local moderators for each major languages:
            - Possible Local Languages (Depends on number of users on mainnet)
                
                English
                
                Chinese
                
                Russian
                
                Ukrainian
                
                Turkish
                
                Indian
                
                Others…
                
        
    - Create Genesis Categories in Forum
        1. Joystream General
            - Sub-Categories
                1. Joy Token
        2. Governance
            - Sub-Categories
                1. Council Reports
                2. Pre-Proposal Discussions
        3. Working Groups
            - Sub-Categories
                1. Storage
                2. Content
                3. Forum
                4. Builders
                5. Apps
                6. Distribution
                7. HR
                8. Marketing
        4. Technical Discussion
        5. Online Videos
            - Sub-Categories
                1. Gleev
        6. Other Topics
        7. Local Languages
        
        Check this link for latest [New Categories List](../Mainnet%20Plans,%20Reports%20and%20Updates/List%20of%20Categories/List%20of%20Categories%20(Initial)/List%20of%20Categories%20(Draft%201)%20c8658c7d57fd4ea3acb45621532a187a.md) presented to Council
        
    - CLI Commands:
        
        `$ joystream-cli forum:createCategory -t "Joystream General" -d "General Discussion that is anything else about Joystream Ecosystem that doesn't fit better in other categories."`
        
        `$ joystream-cli forum:createCategory -t "Governance" -d "Post Council Reports in here"` 
        
        `$ joystream-cli forum:createCategory -t "Working Groups" -d "Post WG Plans, Reports, Summaries and other WG specifics in here"` 
        
        `$ joystream-cli forum:createCategory -t "Technical Discussion" -d "Post technical questions and answers in here. Developers can share ideas in here."` 
        
        `$ joystream-cli forum:createCategory -t "Online Videos" -d "Discussion about video contents uploaded on Apps"` 
        
        `$ joystream-cli forum:createCategory -t "Other Topics" -d "Post non-Joystream related stuffs"` 
        
        `$ joystream-cli forum:createCategory -t "Local Languages" -d "Post non English/ local languages posts"` 
        
    - Create Genesis Threads which can be interacted by genesis forum users
        
        We will most likely create threads about genesis problems to be encountered by genesis users.
        
- **Review [Gitbook Scores](https://joystream.gitbook.io/testnet-workspace/testnet/council-period-scoring/marketers-score) for your Work Group and tell:**
    
    Based on Handbook as we are doing it on testnet, we include chart of forum history since genesis. This will make the chart endless or very long after a long time. I hope we narrow it down like only the last 10 terms (i.e.).
    
    Also regarding number of forum workers, will we scale it based on forum activity? We’re imagining what if we suddenly have millions of users posting millions of posts? Will we hire like 100k posts a day = 5 workers, 1 million posts a day = 10 workers (i.e.)? We think this can be same concern on content group,
    
- **For each position of your WG in the mainnet, incl. the Lead:**
    
    We have not tried computing yet WG score but based on handbook forum moderation, score is based on response time (4-24 hours?) To be honest, we don’t strict ourselves in that time frame, we also moderate old posts/threads.
    
- **If there will be less seats in the WG compared to the number of seats in the current testnet, which people will you hire? Propose your criteria.**
    
    Forum moderation needs active workers, so we will base on their availability and activity
    
- **How would you manage people who didn’t find their place in your WG, but who are still quite experienced?**
    
    We will put them in [pool of trained forum workers](../Forum%20Working%20Group/Training/Forum%20Training%20Pool%20c99ee9018e004047af84a8b9e8aa681f.md). They will be hired once we scaled up workforce.
    
- **Propose a forecast of *capacity* utilization for your WG over time (in terms of capacity required over time/ staff number required over time/ overall budget required over time). For example, for the Storage WG *capacity* will be the total storage space available across all servers.**
    
    As we mentioned above, once there is influx of users from all over the world, we will need to assign local moderators for each region. That is how we imagine forum working group scaling up in terms of number of workers. Aside from that, we want to know if there is need to identify moderator to user ratio. For example 1 moderator for 10k users. So if there will be 1 million users, we will need 100 workers?