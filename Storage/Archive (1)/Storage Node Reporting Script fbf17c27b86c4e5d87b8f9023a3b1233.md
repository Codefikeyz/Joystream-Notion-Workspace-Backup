# Storage Node Reporting Script

- Connect to your server
- Install *wput*

```
sudo apt-get update 
```

```jsx
sudo apt-get install wput
```

- Run

```jsx
nano report.sh
```

- Paste the following text

```jsx
#!/bin/bash

# You need to 
# Install wput service
# Make sure you use the correct folder to upload
# Make sure you set your password
# Make sure you updated your path to joystream storage folder
 
ftpPassword="<ASK STORAGE LEAD FOR THE PASS>"
folderName="0x2bc"
pathToStorageFolder="/root/joystream-storage/"
pathToIfconfig="/usr/sbin/ifconfig"

currentDate="`date +"%Y-%m-%d-%H:%M"`"

ftpIP="87.236.146.74"
ftpLogin="testuser"

echo "Folder name set to "$folderName""

echo "Logging Ifconfig.."
$pathToIfconfig > $currentDate-ifconfig.txt
rm text.txt  2> /dev/null || true
echo "Logging Storage Objects List.."
#Chnage your Storage Folder if needed
ls -l $pathToStorageFolder > test.txt
echo "Prettifying Storage Objects List.."
sed -e 's/\s\+/,/g'  test.txt > $currentDate-objects.txt
echo "Logging network speedtest.."
curl -sL yabs.sh | bash -s -- -fg > $currentDate-speedtest.txt

echo "Sending Files to FTP server.."
#Make sure you use the correct folder to upload
wput $currentDate-ifconfig.txt ftp://testuser:$ftpPassword@87.236.146.74/report/$folderName/$currentDate-ifconfig.txt
wput $currentDate-objects.txt ftp://testuser:$ftpPassword@87.236.146.74/report/$folderName/$currentDate-objects.txt
wput $currentDate-speedtest.txt ftp://testuser:$ftpPassword@87.236.146.74/report/$folderName/$currentDate-speedtest.txt

echo "Removing temp files..."
rm $currentDate-ifconfig.txt
rm $currentDate-objects.txt
rm $currentDate-speedtest.txt
```

Update these variables in the script:

- *ftpPassword*
- *folderName*
- *pathToStorageFolder*
- *pathToIfconfig*

For the *folderName*, use one of those words (based on your Joystream name): 

- [0x2bc](http://87.236.146.74:8000/0x2bc/)
- [alexznet](http://87.236.146.74:8000/alexznet/)
- [GodsHunter](http://87.236.146.74:8000/GodsHunter/)
- [joystreamstats](http://87.236.146.74:8000/joystreamstats/)
- [l1dev](http://87.236.146.74:8000/l1dev/)
- [maxlevush](http://87.236.146.74:8000/maxlevush/)
- [mmx1916](http://87.236.146.74:8000/mmx1916/)
- [yyagi](http://87.236.146.74:8000/yyagi/)

For the *pathToStorageFolder,* use the folder path from your Storage Server config file. It is specified under `-d`  option:

![Untitled](../Archive/Storage%20Node%20Reporting%20Script/Untitled.png)

In order to find *pathToIfconfig,* run 

```jsx
whereis ifconfig
```

For the *ftpPassword*, ask Storage Lead for the password. 

- Once, variables are updated, save file  [report.sh](http://report.sh) file
- Run

```jsx
chmod 777 report.sh
```

- Run the script one time and make sure there is no errors in the log

```jsx
./report.sh
```

- Find your data in the appropriate folder on the FTP server [http://87.236.146.74:8000/](http://87.236.146.74:8000/)
- If everything is ok (new files are uploaded to the server), create *cron* for your script. Change the path to the script, if needed

```jsx
crontab -e
0 12 * * * /root/report.sh
```

- Here we are! Everyday at 12-00 your data will be uploaded to the server [http://87.236.146.74:8000/](http://87.236.146.74:8000/)

### **Update 19 May - In-depth traffic analyzer**

- Install nethogs

```jsx
 apt install nethogs
```

- install go

```jsx
apt install golang-go
```

- Install nethogs parser

Assuming you are a root User, execute following commands

```jsx
cd /root 
```

- create file in the root folder

```jsx
nano [hogs.go](https://github.com/boopathi/nethogs-parser/blob/master/hogs.go)
```

- copy paste the text by the link [https://github.com/boopathi/nethogs-parser/blob/master/hogs.go](https://github.com/boopathi/nethogs-parser/blob/master/hogs.go)
- execute command

```jsx
go build -o hogs hogs.go****
```

- Test whether everything is OK:

Collect traffic consumption for 60 seconds period. Make sure you use correct network interface. In the example, it’s eth0. Your one can be different. Run the following command:

```jsx
timeout 60s nethogs -t eth0 &> /var/tmp/nethogs.log
/root/hogs -type=pretty /var/tmp/nethogs.log > /var/tmp/nethogs-pretty.log
cat /var/tmp/nethogs-pretty.log
```

Output should look like this. The table shows received and sent traffic in KB per process per 60 seconds period:

```xml
root@frhb68736ds:~# cat /var/tmp/niceView.log
Output for file = /var/tmp/nethogs2.log

                     213.246.57.91:56314	      0.56	      1.42	                                    root
                     213.246.57.91:46859	      0.00	      0.01	                                    root
                      213.246.57.91:8200	      0.00	      0.00	                                    root
/root/.volta/tools/image/node/14.18.0/bin/node	      0.17	      0.17	                                    root
                        sshd:_root@pts/0	      0.38	      0.23	                                    root
                     213.246.57.91:49560	      0.06	      0.06	                                    root
                     213.246.57.91:25564	      0.00	      0.00	                                    root
                             unknown_TCP	      0.00	      0.00	                                    root
                    **/root/joystream-node	    15558.65	    15561.75**	                                    root
                     213.246.57.91:21242	      0.00	      0.00	                                    root
                        213.246.57.91:23	      0.00	      0.00	                                    root
                       213.246.57.91:443	      0.35	      0.36	                                    root
                     213.246.57.91:42124	      0.00	      0.00	                                    root
                      213.246.57.91:4000	      0.01	      0.01	                                    root
                      213.246.57.91:8087	      0.00	      0.00	                                    roo
```

- Open  [report.sh](http://report.sh) script.

```jsx
nano report.sh
```

- Add the following at the end of file. Script will measure traffic consumption during 24 hours period. Make sure you use correct network interface. In the example, it’s eth0.

```bash
echo "Analyzing traffic consumption.."
if pidof -x "nethogs" >/dev/null
then
    echo "Process already running"
else
     nethogs -t eth0 &> /var/tmp/nethogs.log &
fi

/root/hogs -type=pretty /var/tmp/nethogs.log > /var/tmp/nethogs-pretty.log
wput /var/tmp/nethogs-pretty.log ftp://testuser:$ftpPassword@87.236.146.74/report/$folderName/$currentDate-nethogs-pretty.txt
rm  /var/tmp/nethogs-pretty.log

#if file size more than 1 GB we will delete the log and re-launch the process

if [ -n "$(find "/var/tmp/nethogs.log" -prune -size +1000000000c)" ]
then
    echo 'Nethogs LOG file is larger than 1 GB. Old log file will be removed. New lod file will be created'
    ps -ef | grep 'nethogs' | grep -v grep | awk '{print $2}' | xargs -r kill -9
    rm /var/tmp/nethogs.log
    nethogs -t eth0 &> /var/tmp/nethogs.log & 
else
    echo 'Nethogs LOG file is lower than 1 GB. Do nothing'
fi
```

- Save  [report.sh](http://report.sh) script.