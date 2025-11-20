# Joystream Role Bot

**Developer**: Create

**Maintainer**: Dzidex

**Version**: 1.0.1

**Background:** https://github.com/Joystream/discord-bot/issues/5

**Feature**: Discord users can claim Joystream discord server roles, including Founding Member role, Council Member role, Working Group roles and Creator roles by linking their discord accounts to Joystream on-chain memberships. The synching process will happen at a specified interval.

**How to use**

The bot will automatically synch on-chain roles to all discord users that have entered their discord username in their Pioneer membership profile.

Below is the list of available commands.

- `/who_is`
    
    List member id and on-chain roles of the given discord account
    
    **discord_handle:** the discord Username of which you wish to display information, must start with`@` 
    
    example: `/who_is discord_handle @Chaos77`
    
- `/list_role_members`
    
    List the  discord usernames who have the specified discord role
    
    **discord_role**: The command will display users with this role, must start with `@`
    
    example: `/discord_role discord_role @FoundingMember`
    
- `/status`
    
    Displays the following information
    
    - on-chain roles that are empty
    - what version of bot is running
    - last block where synchronization happened

- `/help`
Link the user to this help page.

**Setup**

In order to start the discord bot server and connect it to the Joystream discord server, the admin must follow the next steps.

- Configure the config.ts file to map role ids between the server and bot
- Create an application on discord developer portal, create a bot with permissions `2415937536` and authorize it.
- Configure the env file.
SERVER_TOKEN = discord bot token
SERVER_ID = discord server id
VERSION= version number
QUERY_NODE= URL of Joystream QN
RPC_URL= URL of Joystream RPC
SYNCH_TIME = time of synchronization in minutes
- Deploy the bot server