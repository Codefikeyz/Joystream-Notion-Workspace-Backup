# How-to setup Joystream CLI (Windows)

**Note: This tutorial is intended for Windows Users**

1. Download node.js and NPM Installer from this link “ [https://nodejs.org/en/download/](https://nodejs.org/en/download/) “

![1.png](How-to%20setup%20Joystream%20CLI%20(Windows)/1.png)

1. Install node.js and NPM using downloaded file

![2.png](How-to%20setup%20Joystream%20CLI%20(Windows)/2.png)

- ‘Welcome to the Node.js Setup Wizard’ will show – click **Next**
- On the next screen, review and understand the license agreement. If you agree - click **Next.**
- The installer will prompt you for the installation location. Leave the default location, unless you want to install it somewhere else – then click **Next.**
- The wizard will let you select components to include or remove from the installation. Again, unless you have a specific need, accept the defaults by clicking **Next.**
- Click the **Install** button to run the installer. When it finishes, click **Finish.**

1. Verify Installation of node.js and NPM in cmd
- Open cmd (command prompt)
- Check version of node.js installed

```powershell
node -v
```

- Check version of NPM installed

```powershell
npm -v
```

- If cmd result is similar in below picture, then go to next process

![3.png](How-to%20setup%20Joystream%20CLI%20(Windows)/3.png)

1. Download Git cmd installer from this link “ [https://git-scm.com/download/win](https://git-scm.com/download/win) “

![4.png](How-to%20setup%20Joystream%20CLI%20(Windows)/4.png)

1. Install Git cmd using downloaded file

![6.png](How-to%20setup%20Joystream%20CLI%20(Windows)/6.png)

- Review and understand the license agreement - Click Next
- The wizard will let you select components to include or remove from the installation. Unless you have a specific need, accept the defaults by clicking **Next.**
- Click the **Install** button to run the installer. When it finishes, click **Finish.**

1. Install Joystream CLI
- Open cmd (command prompt)
- Type below command and enter

```powershell
npm install -g @joystream/cli
```

![7.png](How-to%20setup%20Joystream%20CLI%20(Windows)/7.png)

When it finishes, cmd shows **0 vulnerabilities** like in picture above

1. Verify Installation of CLI 
- Type below command and enter

```powershell
joystream-cli --version
```

- If cmd result is similar in below picture, then go to next process

![7.png](How-to%20setup%20Joystream%20CLI%20(Windows)/7%201.png)

1. Configure CLI
- Set the correct Joystream node websocket endpoint by typing below command

```powershell
joystream-cli api:setUri
```

- You will be given several choices. Select below endpoint

```powershell
wss://rpc.joystream.org:9944
```

- Import your json file by typing below command

```powershell
joystream-cli account:import --backupFilePath=backupFilePath
```

- backupFilePath = “Path File of Json File” + “\” +”File Name of Json File” + “.json”
- sample:   C:\Users\account.json
- *****so whole command will be:

![9.png](How-to%20setup%20Joystream%20CLI%20(Windows)/9.png)

- Just answer what the cmd asks.
- You will be prompted to set new account name
- You will be prompted to set new password.

1. If everything is OK, below picture will show “ New account successfully created! “

![10.png](How-to%20setup%20Joystream%20CLI%20(Windows)/10.png)

1. Congratulations! You can now use the CLI command. Follow this link for list of CLI commands. 
- [https://github.com/Joystream/joystream/tree/master/cli#joystream-cli-accountimport](https://github.com/Joystream/joystream/tree/master/cli#joystream-cli-accountimport)