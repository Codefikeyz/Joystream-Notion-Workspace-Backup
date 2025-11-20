# How-to setup Joystream CLI (Linux)

**Note: This tutorial is intended for Linux Users**

1. **Install node.js on Linux**
    
    The Linux operating system has hundreds of different distributions because of the diversity it provides. And users love to customize and harness different versions’ specific functionalities using distinct distributions.
    
    This guide assumes that you are using Ubuntu 20.04. Before you begin, you should have a non-**root** user account with `sudo`privileges set up on your system. You can learn how to do this by following the [Ubuntu 20.04 initial server setup tutorial](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04)
    
    **Step 1:**
     Open your terminal or press Ctrl + Alt + T.
    
    ![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled.png)
    
    **Step 2:**
     To install node.js use the following command:
    
    ***sudo apt install nodejs***
    
    ![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%201.png)
    
    **Step 3:**
     Once installed, verify it by checking the installed version using the following command:
    
    ***node -v** or **node –version***
    
    ![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%202.png)
    

**Note:**

It is recommended to install Node Package Manager(NPM) with Node.js. NPM is an open source library of Node.js packages.

To install NPM, use the following commands:

***sudo apt install npm***

***npm -v** or **npm –version***

1. **Install Joystream CLI**

- Open your terminal or press Ctrl + Alt + T.
- Type below command and enter

```powershell
npm install -g @joystream/cli
```

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%203.png)

When it finishes, terminal shows **0 vulnerabilities** like in picture above

1. **Verify Installation of CLI** 
- Type below command and enter

```powershell
joystream-cli --version
```

- If terminal result is similar in below picture, then go to next process

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%204.png)

1. **Configure CLI**
- Set the correct Joystream node websocket endpoint by typing below command

```powershell
joystream-cli api:setUri
```

- You will be given several choices. Select below endpoint

```powershell
wss://rpc.joystream.org:9944
```

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%205.png)

**Create a new account**

```powershell
joystream-cli account:create
```

- If it asks query node uri, set below one.

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%206.png)

- Just answer what the terminal asks.
- You will be prompted to set new account name
- You will be prompted to set new password.
- If everything is OK, below picture will show “ New account successfully created! “

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%207.png)

**Importing Account**

- Import your json file by typing below command as long as you have a backup file

```powershell
joystream-cli account:import --backupFilePath=backupFilePath
```

- backupFilePath = “Path File of Json File” + “/” +”File Name of Json File” + “.json”
- sample:   Home/Username/account.json
- *****so whole command will be:

![Untitled](How-to%20setup%20Joystream%20CLI%20(Linux)/Untitled%208.png)

1. **Congratulations! You can now use the CLI command. Follow this link for list of CLI commands.** 
- [https://github.com/Joystream/joystream/tree/master/cli#joystream-cli-accountimport](https://github.com/Joystream/joystream/tree/master/cli#joystream-cli-accountimport)