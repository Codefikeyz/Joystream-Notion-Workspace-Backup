# Setting up Joystream Development Environment in Windows Computer

[Настройка среды разработки Joystream на компьютере с Windows](Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D1%81%D1%80%D0%B5%D0%B4%D1%8B%20%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B8%20Joystream%20%D0%BD%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%B5%203932125ac4104430a8e049c0dc34a59a.md)

[Налаштування середовища розробки Joystream на комп'ютері з Windows](Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/%D0%9D%D0%B0%D0%BB%D0%B0%D1%88%D1%82%D1%83%D0%B2%D0%B0%D0%BD%D0%BD%D1%8F%20%D1%81%D0%B5%D1%80%D0%B5%D0%B4%D0%BE%D0%B2%D0%B8%D1%89%D0%B0%20%D1%80%D0%BE%D0%B7%D1%80%D0%BE%D0%B1%D0%BA%D0%B8%20Joystream%20%D0%BD%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BF%200ed76a8cd3a74dceb3d738669ce9727b.md)

# **Setting up Joystream Development Environment in Windows Computer.**

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled.png)

# **Problem Statement**

In our Joystream community, it was observed that there are many builders joining our community with windows computer resources, due to a lack of Mac or Unix computer system with them, they were unable to contribute to our community. 

# Overview

Getting windows machine ready for setting up Joystream development environment. So that our community users with windows computers can start building application. 

## Setup processes

1. **Install WSL in Windows** 
2. Install Ubuntu in Windows 
3. Install VS Code 
4. Clone the Joystream pioneer from GitHub 
5. Run Joystream pioneer in local host.

## 1. Install WSL in Windows

Kindly follow this document to complete WSL installation in your windows computer.

[https://docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install)

# 2. Install Ubuntu

o Go to Microsoft Store search for Ubuntu 

 

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%201.png)

Proceed with the setup

Now, enter **sudo apt update && sudo apt upgrade**  to complete the setup.

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%202.png)

# 3. Install VS Code

The below web document has a complete VS Code setup guide, kindly go thru it and follow the guidelines for completing the installation of VS Code.

[https://code.visualstudio.com/docs/setup/windows](https://code.visualstudio.com/docs/setup/windows) 

# 4. Configure WSL in VS Code

Open VS Code, Go to extension search for Remote WSL

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%203.png)

Complete the installation 

Now close the VS Code and open again.

Open the New WSL window from VS Code and open a new terminal 

[**https://github.com/Joystream/pioneer#quickstart](https://github.com/Joystream/pioneer#quickstart)   read this link carefully and try to understand the structure.** 

# 5. Clone the Joystream pioneer from GitHub

From VS Code WSL terminal clone the Joystream pioneer repository 

[https://github.com/Joystream/pioneer.git](https://github.com/Joystream/pioneer.git)

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%204.png)

**This is** a **very important step,** once it is cloned . Change the directory to pioneer.

type yarn and enter, on the successful installation you should be able to see the following screen.

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%205.png)

Now execute a yarn build for this close the VS Code go to your windows powershell navigate to the pioneer directory and execute this yarn build. 

## 6. Run Joystream pioneer in local host.

 ############    Create .env File and include the following code     ############

REACT_APP_TESTNET_NODE_SOCKET=wss://rpc.joystream.org:9944
REACT_APP_TESTNET_QUERY_NODE=https://query.joystream.org/graphql
REACT_APP_TESTNET_QUERY_NODE_SOCKET=wss://query.joystream.org/graphql
REACT_APP_TESTNET_MEMBERSHIP_FAUCET_URL=https://18.234.141.38.nip.io/member-faucet/register

Add the .env file in the pioneer/packages/ui  

Now execute yarn start 

[http://localhost:8080/#/settings](http://localhost:8080/#/settings)
and choose `Joystream-Testnet` from the drop-down!

![Untitled](../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%206.png)

Here you go, now you can start building from your windows computer! 

# Conclusion

Even after this, you may run into some minor issues, kindly double-check the steps. Still unable to get a solution, feel free to ask us in the discord.