internetworking
===============

### User Guide

This user guide shows the steps on how to setup the Raspberry PIs for this project from the beginning.

1.	Format SD card to FAT
2.	Download NOOBS from raspberrypi.org/downloads
3.	Extract files
4.	Copy the extracted files onto the SD card that you just formatted, so that this file is at the root directory of the SD card
5.	Boot the Pi
6.	Choose the Raspbian OS > Connect to WiFi > Choose Language and Keyboard > Install
 
7.	Run sudo apt-get update on the terminal
8.	Install VNC Connect by running command sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer
9.	Enable VNC Server by Select Menu > Preferences > Raspberry Pi Configuration > Interfaces > Ensure VNC is Enabled.
10.	Install VNC Viewer on your machine to connect remotely.
11.	Enter the IP address of the PI
 
12.	Install Node-red by running the command
bash <(curl -sL https://raw.githubusercontent.com/node-red/raspbian-deb-package/master/resources/update-nodejs-and-nodered)  
13.	Wait for it to install
 
14.	Install as a global module by running the command
Sudo npm install -g --unsafe-perm node-red
 
15.	Wait until it is done
 
16.	Install SQLite database by running the command
sudo apt-get install sqlite3
  
17.	Wait until it is done  
18.	Install SQLite DB Browser using the command
sudo apt-get install sqlitebrowser
 
19.	Wait until it is done
20.	Start node-red by running the command
node-red-start 
 
21.	Run the below command to autostart Node-red at every boot
sudo systemctl enable nodered.service
 
22.	Open node-red by Opening a browser > type localhost:1880
 
23.	There is currently no Project feature so we cannot clone the repository
 
24.	Reboot the PI
25.	To setup projects feature, navigate to the below path > right-click on settings.js file > Open With… >
 
26.	Select Text Editor > Ok   
27.	Go all the way to the bottom of the file and change false to true > Save > Close  
28.	Restart node-red
node-red-stop 
node-red-start 
  
29.	When projects feature is enabled, we can pull repositories from GitHub > Clone repository 
 
30.	Enter username and email
l  
31.	Enter URL of repository https://github.com/carmen-villamor/internetworking_project > Clone Project
  
32.	You have pulled the master branch which is the broadcasting node’s branch. If you are after the receiver branch, please skip to Step 37.  
33.	There some nodes missing because you need to install the dependencies. Click the Settings menu > Manage palette 
 
34.	Install the sense-hat nodes  
35.	Install SQLite 
 
36.	After installation, it should look like this  
37.	To pull Receive branch, open Settings > Click the history tab > Commit History > Create a Receiver branch
 
38.	Select the receiver branch > Select Push/Pull icon > Select Receive branch from repository
 
39.	Pull the branch 
 
40.	If you get this error message > Select show merge conflicts  
41.	Select flow.json > Accept all changes  / merge conflicts 
42.	You will then get the flow setup for the miner nodes
 
43.	Debug window currently shows the output of the CONVERT node  
44.	To open the database of the blockchain list > Go to the directory > Right-click on blockchianlist > DB Browser for SQLite
 
45.	You can the browse the DB  

