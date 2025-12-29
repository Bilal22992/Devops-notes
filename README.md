# Dec 17 2025 
## Linux Commands, Linux directories, Absolute & Relative paths
### Linux Commands
ls - The most frequently used command in Linux to list directories<br>
pwd - Print working directory command in Linux <br>
cd - Linux command to navigate through directories<br>
mkdir - Command used to create directories in Linux<br>
mv - Move or rename files in Linux<br>
cp - Similar usage as mv but for copying files in Linux<br>
rm - Delete files or directories<br>
touch - Create blank/empty files<br>
ln - Create symbolic links (shortcuts) to other files<br>
clear - Clear the terminal display<br>
cat - Display file contents on the terminal<br>
echo - Print any text that follows the command<br>
less - Linux command to display paged outputs in the terminal<br>
man - Access manual pages for all Linux commands<br>
uname - Linux command to get basic information about the OS<br>
whoami - Get the active username<br>
tar - Command to extract and compress files in linux<br>
grep - Search for a string within an output<br>
head - Return the specified number of lines from the top<br>
tail - Return the specified number of lines from the bottom<br>
diff - Find the difference between two files<br>
cmp - Allows you to check if two files are identical<br>
comm - Combines the functionality of diff and cmp<br>
sort - Linux command to sort the content of a file while outputting<br>
export - Export environment variables in Linux<br>
zip - Zip files in Linux<br>
unzip - Unzip files in Linux<br>
ssh - Secure Shell command in Linux<br>
service - Linux command to start and stop services<br>
ps - Display active processes<br>
kill and killall - Kill active processes by process ID or name<br>
df - Display disk filesystem information<br>
mount - Mount file systems in Linux<br>
chmod - Command to change file permissions<br>
chown - Command for granting ownership of files or folders<br>
ifconfig - Display network interfaces and IP addresses<br>
traceroute - Trace all the network hops to reach the destination<br>
wget - Direct download files from the internet<br>
ufw - Firewall command<br>
iptables - Base firewall for all other firewall utilities to interface with
apt, pacman, yum, rpm - Package managers depending on the distribution<br>
sudo - Command to escalate privileges in Linux<br>
cal - View a command-line calendar<br>
alias - Create custom shortcuts for your regularly used commands<br>
dd - Majorly used for creating bootable USB sticks<br>
whereis - Locate the binary, source, and manual pages for a command<br>
whatis - Find what a command is used for<br>
top - View active processes live with their system usage<br>
useradd and usermod - Add a new user or change existing user data<br>
passwd - Create or update passwords for existing users<br>

### Linux Directories
/ (Root): The top of the entire file system; everything branches from here.<br>
/bin: Essential user command binaries (e.g., ls, cp).<br>
/sbin: System binaries for administration (e.g., mount), typically for root.<br>
/etc: System-wide configuration files.<br>
/home: Contains individual user's home directories (e.g., /home/yourname).<br>
/root: The home directory for the superuser (root).<br>
/lib & /lib64: Essential shared libraries for programs.<br>
/usr: User programs, libraries, and documentation.<br>
/var: Variable data like logs, mail, and spool files.<br>
/tmp: Temporary files, often cleared on reboot.<br>
/dev: Device files representing hardware (e.g., disks, terminals).<br>
/proc: Virtual filesystem with process and kernel info.<br>
/opt: Optional or third-party software.<br>
/boot: Files needed to start the system (kernel, bootloader).<br>
/mnt, /media: Mount points for temporary or removable media.<br> 
<img width="728" height="590" alt="image" src="https://github.com/user-attachments/assets/4c81659d-89fb-45b0-b4a6-f7b6e837da97" />

### Relative Path
Relative is the path where if we are in a directory and then give path of the files or directories within it. <br>For Example if we are in /home and want to go /home/moon so we will give cd /moon.

### Absolute Path
Here we give the complete path to the file or directories <br> . For example to reach to /home/moon we will give the path /home/moon

## Create 2 users, 2 groups, assign sudo & group membership
### Linux Users
Every person who interact with linux has a user or associated with a user. 
The main or the super user is the root.
Each user has a user id UID.
**Root** has a UID 0. <br>
**System file** and directories running **background processes** have UID between 1-999<br>
**Normal Users** have UID 1000+.<br>
Key Files Include 
1) /etc/passwd containing user and group info and 
2) /etc/shadow containing encrypted  user passwords
### Linux Groups
it is a collection of users. We can give permissions to a group and can add users to it having the same permission instead of giving them individually.<br>
Each group has a unique group id.
There are two types of groups <br>
1)**Primary Group** which is created right after the user is being created with the name of the user . <br>
For example if i created a admin user then a group named admin will be created automatically.<br>
2)**Secondary Group** it is the group where we can add users to have those access.<br> For example if we want a user to have sudo access then we add it to sudo group.

Key file here are
**/etc/group**


# Creating users and groups and then adding them to groups
In Linux we create users with the command <br>
**adduser user1** <br>
This command creates the user and then also creates a group associated with it. <br>
we can create seperate groups with the command <br>
**addgroup group1** <br>
after we can add users to the group by using the command<br>
**usermod -aG groupname username**<br>

For adding user to sudo use <br>
**usermod -aG wheel username**
For creating no bash user use the command <br>
**usermod -s /sbin/nologin**

"**Command**     **Best Used For...**         **Key Feature**<br>"
**ls**"  	        "Finding out what files exist	     Shows directory contents.<br>
**cat**            Displaying short files	       Dumps everything to the screen.<br>
**head**	  Checking file headers/start	     Shows the top 10 lines.<br>
**tail**	  Monitoring logs	               Shows the bottom 10 lines.<br>
**more**	  Basic page-by-page viewing	     Forward scrolling only.<br>
**less**	  Reading any large file	       Interactive; scroll up, down, and search.<br>
**zcat**	  Viewing .gz files	              Views compressed data directly.<br>




<img width="1349" height="824" alt="image" src="https://github.com/user-attachments/assets/4a5dc8b6-f41b-46f1-bed5-ab29445ab44b" />

<img width="808" height="116" alt="image" src="https://github.com/user-attachments/assets/1eb05650-792a-4d77-85ec-b23906ccb9b1" />
<img width="485" height="99" alt="image" src="https://github.com/user-attachments/assets/ac192bae-ad04-4162-a9b3-bcf529bdb89c" />
<img width="336" height="103" alt="image" src="https://github.com/user-attachments/assets/c6b32fff-ce74-4d03-bf66-4cdf2f0b1ad7" />
<img width="905" height="826" alt="image" src="https://github.com/user-attachments/assets/c96944ee-3532-4fb6-924e-1fa252b3a7be" />
<img width="791" height="159" alt="image" src="https://github.com/user-attachments/assets/b6524ab8-6be0-4e79-8715-88bcf59e08b8" />




# 18 Dec 2025
## > , >> , wc, du -sh *

### >
  it is use to write to the file but the text in the file will be overwritten. For Example 
  <img width="693" height="160" alt="image" src="https://github.com/user-attachments/assets/a8a555c2-4642-4295-9f5c-d9a5c8764e93" />

### >>
it is used to write to the file. In this case it appends the data to the data already present in file.
<img width="591" height="193" alt="image" src="https://github.com/user-attachments/assets/4e33b2a4-2bfa-4832-b387-4f5d40411e30" />

### wc
it is used for line ,word and byte count in the file . in byte count it gives all the spaces and /n(end of line) as well. For Example
<img width="545" height="232" alt="image" src="https://github.com/user-attachments/assets/0c878429-0c2d-4078-bfa6-fc1d22f22013" />

### du -sh *
it is used for check the disk usage. If we run du only it just gives a number which is a bit hard to understand. du -s will give the disk usage and also prevent it from listing every folder. du -h will give the human readable form like in kbs and du -sh * will give the data consumed by each and every file and folder.
<img width="958" height="275" alt="image" src="https://github.com/user-attachments/assets/13cb8289-736a-41f7-aa85-9a2345989bf7" />


## Pipe
it is used to combine the commands. For example if we want to read a file using cat and then want to find the h letter and then count the number of that letter we can combine all these commands in a single line as follows. 
<img width="674" height="240" alt="image" src="https://github.com/user-attachments/assets/f53276fe-36bf-4844-9cbf-56387d8a7d6e" />

## grep, egrep, zgrep

### grep (global regular expression print)
it is used for searching a file. it is based on BRE ( Basic Regular Expression) . Main flag here are -i -v -n. Practical work is as follows.

grep -i :  it is ignore case. it just ignores the casing and prints the matching letter of both cases.
grep -v : it is invert case where it ignore the lines where matching data is found.
grep -n : it print the data with the line number it is being found. Practical work is as follows 
<img width="972" height="263" alt="image" src="https://github.com/user-attachments/assets/591d83c9-d25c-4c37-aa90-6f9c57be2405" />

### egrep
it is extended case for grep for the special characters like | or + etc , as in grep they are read as normal characters so to give them power like pipe symbol we have to use backslashes \. Practical work is as follows.
<img width="715" height="203" alt="image" src="https://github.com/user-attachments/assets/63c2aca2-ce7c-427b-a813-48dadb9ef285" />

### zgrep 

it is used to study the .gz file data as normal grep is not able to get the .gz data so we have to use zgrep. Practical work is as follows
<img width="630" height="219" alt="image" src="https://github.com/user-attachments/assets/89cc56f9-c8bd-4bd7-95f1-b118b59b8676" />

## sort, cut, uniq, awk, sed

### sort 
it is used to sort the data in a file. it has different flags. simple sort sorts the data in ascending order as follows
<img width="586" height="413" alt="image" src="https://github.com/user-attachments/assets/bc070eaa-73fe-403a-bd33-6131dbc5c7a1" />
sort -r: it sorts in reverse form as follows 
<img width="549" height="205" alt="image" src="https://github.com/user-attachments/assets/84c4a89d-75bd-42b7-b926-a0468ddfd636" />

sort -u: it sorts and removes the dublicates as follows
<img width="745" height="350" alt="image" src="https://github.com/user-attachments/assets/35017369-261e-4f03-80d9-2330f8259895" />

### cut 
it is used to extract column data from a file. it has two flags one is -d for choosing the delimiter and the other is -f for choosing the column number. Practical work is as follows
<img width="690" height="731" alt="image" src="https://github.com/user-attachments/assets/b9ebe6b0-43f7-4a44-919e-e503d4ac04ad" />

### uniq
it is used to see the dublicate entries and works only if the entries are consective or nect to each other. it has two flags one is -c for counting the dublicate entries and -d for only showing the dublicate entries. practical work is as follows

<img width="820" height="569" alt="image" src="https://github.com/user-attachments/assets/2c5b96fe-6b0e-4e75-b6df-0027bcebe5f4" />

### sed 
it is the streamline editor. it is used to replace values in a file without opening it. it has two arguments one is s for subsitute and other is g for global to replace all the values in a line not just first one.
<img width="466" height="311" alt="image" src="https://github.com/user-attachments/assets/fd5363be-3241-448c-a4a9-2b573881fadc" />
it is also used to delete a entry or a line with giving the argument in single quote like '1d' where 1 is line number and d is for delete. Practical work is as follows
<img width="583" height="305" alt="image" src="https://github.com/user-attachments/assets/ea1f2638-c391-4941-b0e3-96d226767ba2" />

### awk 
it is similiar to cut and is used to extract columns. in simple cases where columns are seperated by spaces it detects them automatically but if the seperator are something like : then we have to speecify using -F ":" flag . Practical example is as follows

<img width="579" height="525" alt="image" src="https://github.com/user-attachments/assets/805f6b8c-d235-4efc-ad66-fa362a650c5b" />



# 19 Dec 2025

## tar, tar.gz, zip, rar

### tar  
it is commonly used in linux to move folders. it does not compress the folder and its size is same as the original file size but it makes the folder into a single file and makes it easy to move. Moreover it retains the ownership of folder which is lost in case of zip.

Practical work is as follows:-   
**creating .tar file**
<img width="805" height="295" alt="image" src="https://github.com/user-attachments/assets/02dc580a-33e8-481f-87e4-bfade7d0b2eb" />
**Extracting .tar file**
<img width="675" height="190" alt="image" src="https://github.com/user-attachments/assets/16594804-14cd-4745-85d4-ddd79ac9a8df" />

### tar.gz 
it is used to compress the tar files. which means first files are being made .tar and then passes through gzip . it is used to compress the files.
**creating .tar.gz files** 
<img width="736" height="115" alt="image" src="https://github.com/user-attachments/assets/c6853c45-a658-4257-b716-388822414908" />


**Extracting .tar.gz files**
<img width="680" height="205" alt="image" src="https://github.com/user-attachments/assets/6bf8617b-cbaa-459c-abdf-d68a454958f5" />

### zip
it is used to compress the folders. unlike tar here it does not retain ownership data and archives and compresses at the same time.
**Creating zip files**
<img width="779" height="139" alt="image" src="https://github.com/user-attachments/assets/3485b172-3e5e-408f-95d3-8474408fc19a" />


**Extracting zip files**
<img width="868" height="225" alt="image" src="https://github.com/user-attachments/assets/6ba461a7-d84f-4379-90d1-4a6c76355d41" />


### unrar rar
it is not present in linux repositories and we have to manually install it. it first require epel to install the rar. To install epel we run the command <br>yum install -y epel-release<br>
then to install unrar we run  <br>
yum install -y unrar
<img width="1386" height="287" alt="image" src="https://github.com/user-attachments/assets/625cbc32-9885-4b1e-bd7c-7e4c95d62486" />

<img width="1453" height="310" alt="image" src="https://github.com/user-attachments/assets/b5a416de-2521-4c08-bc98-44673f2b9768" />

## Hard links / Soft links

1. Hard Links<br>
A hard link is a direct mirror of the original file. It points to the exact same Inode as the source file.<br>

**Behavior:** If you delete the original file, the hard link still works and contains all the data, because the data isn't deleted until all hard links to that Inode are gone. <br>

**Permissions:** Changes made to the data in one file reflect in all hard links because they share the same physical space on the disk.<br>

**Limitations:**

Cannot link directories.<br>

Cannot cross different filesystems (e.g., you can't hard link a file from a USB drive to your local hard drive).<br>

**Command:** ln [original_file] [link_name].<br>

2. **Soft Links** (Symbolic Links / Symlinks)<br>
A soft link is more like a Windows shortcut. It is a separate file that contains the path to the original file, but it has its own unique Inode.<br>

**Behavior:** If you delete the original file, the soft link becomes "broken" (dangling) because the path it points to no longer exists.<br>

**Permissions:** A soft link can have different permissions than the original file, though usually, it inherits the behavior of the source.<br>

**Advantages:**<br>

Can link to directories.<br>

Can link to files on different filesystems or partitions.<br>

**Command:** ln -s [original_file] [link_name].


### readlink 
it is used to check the soft link file. Command for this is readlink -f filename 
<img width="1195" height="272" alt="image" src="https://github.com/user-attachments/assets/27390c8c-2d26-4c68-906a-9da9b3752985" />

### vi/Vim 
it is a linux based editor to manipulate files.
some of the basic commands of vi/vim are :

1. The Essentials <br>

(Getting In and Out)If you get stuck, press Esc a few times to return to Normal Mode.<br>
i: Enter Insert Mode (start typing at the cursor).<br>
Esc: Return to Normal Mode.:w: Save (write) the file.<br>
:q:Quit.<br>
:wq or :x: Save and quit.<br>
:q!: Quit without saving changes.<br>
2. Navigation (Normal Mode)While you can use arrow keys, these shortcuts keep your hands on the "home row.<br>
"CommandAction h j k l Move Left, Down, Up, Right <br>
w / bJump to start of next word / previous word<br>
0 (zero)Jump to start of the line<br>
$Jump to end of the line<br>
gg Go to the first line of the document<br>
G Go to the last line of the document<br>
#G Go to line number#(e.g., 10G goes to line 10)<br>
3. Editing (Normal Mode)<br>
You don't need to be in Insert Mode to delete or change text.<br>
x: Delete a single character.<br>
dd: Delete (cut) the entire line.<br>
dw: Delete from cursor to the start of the next word.<br>
yy: Copy (yank) the current line.<br>
p: Paste the copied/cut text after the cursor.<br>
u: Undo the last action.<br>
Ctrl + r: Redo.<br>
4. Search and Replace/pattern:<br>
Search for "pattern" (press n for next match, N for previous).<br>
:%s/old/new/g: Replace all occurrences of "old" with "new" in the entire file.<br>
:%s/old/new/gc: Replace all occurrences but ask for confirmation first.<br>
5. Visual Mode (Selecting Text)<br>
v: Enter Visual Mode to highlight character by character.<br>
V: Enter Visual Line Mode to highlight entire lines.<br>
d or y: Once text is highlighted, press d to delete or y to copy.<br>
Pro Tip: The "Verb + Noun" GrammarVim commands often follow a pattern: (Number) + (Action) + (Movement).<br>
3dd: Delete 3 lines.d2w: Delete 2 words.<br>
y$: Copy from the cursor to the end of the line.<br>

# 22Dec2025

## /etc/hosts /etc/resolv.config

### /etc/hosts
it is used for mapping ip adresses to their domain name. it is custom name resolution. For Example we can map localhost ip to google.com.  Practical example is as follows

<img width="775" height="231" alt="image" src="https://github.com/user-attachments/assets/5e6e6642-f78a-4c52-8b9f-f5b831ed722c" />

### /etc/resolv.config

if a domain is not found in /etc/hosts then it will look for named servers in /etc/resolv.config.  Practical example is as follows 
<img width="990" height="237" alt="image" src="https://github.com/user-attachments/assets/9bff2beb-f6e8-4ef5-bdcb-7c3b40b85533" />

## SSH password-less login

we generated key using keygen on the client OS and then added the port 2222 to the port forwarding. after that we ran the command mentioned in practical work also on the CLient OS and it let us login without password.
<img width="1176" height="200" alt="image" src="https://github.com/user-attachments/assets/90ca807e-dd48-4d3e-80c5-3c53dfb7a1f3" />

## Curl
it is used to transfer data to or from server using various protocols http , ftp , https .
curl is used in checking NAT configurations 
or checking website headers like curl http://www.google.com which will give header responses without any downloading.

## TCPDUMP 
it is used to monitor network traffic . Common Commands are 
List Interfaces: See which network adapters are available (e.g., eth0, enp0s3): sudo tcpdump -D <br>

Simple Capture: Monitor all traffic on a specific interface: sudo tcpdump -i eth0 <br>

Stop After N Packets: Limit the capture so it doesn't scroll forever: sudo tcpdump -c 10 -i eth0 <br>




# 23 Dec 2025

## Change timezone, NTP vs Chrony, chronyd setup

### Change timezone
it is done through timedatectl 
TO check list of available timezones we run the command **timezonectl list-timezones**
Similiarly to set the timezone we run the command **timezonectl set-timezone Area/Region**
TO check the timezone we run the command **timezonectl**

<img width="846" height="166" alt="image" src="https://github.com/user-attachments/assets/fb48901c-ec8d-49fb-880d-02edb4801e44" />
<img width="726" height="248" alt="image" src="https://github.com/user-attachments/assets/45c83c41-7caa-4f6d-92a2-6b561882afa3" />

### NTP vs Chrony ChronD setup
NTP and Chrony are the utilities to synchronise the timezones across the devices over the network.<br>
NTP is an old utility and is depreciated. It is also not downloadable now in CentOS
<img width="1045" height="99" alt="image" src="https://github.com/user-attachments/assets/20436cfe-2a1b-4f16-8d8f-b717922f1e0c" />

Meanwhile Chrony is used now for time synchronization purposes. 
Practical work is as follows
<img width="989" height="401" alt="image" src="https://github.com/user-attachments/assets/c38a3978-6ecf-4bf3-890d-a30b0dec1038" />


### selinux
it is used to manage security for linux. it has three modes enforcing , permissive and disabled.<br>
Enforcing is the highlevel security and it strictly follows all the policies.<br>
permissive is the one which does not blocks any action and it just logs.<br>
Disabled is the one with no security. <br>
For Temporary change we have two option permissive , enforcing . we have commands setenforce 0 and setenforce 1 for this.<br>
but for Permanent we have to change it in the config file which is located in /etc/selinux/config .

### break password
for this we have to restart our OS and enter into grub menu when when OS starts by clicking ESC<br>
after that we have to type e to enter edit mode<br>
in the edit mode we have to change ro to rw and init=/bin/bash <br>
after that we have to type ctrl+X and it will lead to a terminal.<br>
After that we will create a /.autorelabel file using touch /.autorelabel <br>
After this we will type passwd and enter the new password.
after that we have to run exec /sbin/init and login using username and new password.

### SCP and Rsync

**SCP**
SCP is used to copy files and folders to remote. We can send files from one operating system to another using SCP. Practical work is as follows.
<img width="1164" height="89" alt="image" src="https://github.com/user-attachments/assets/91afaa66-e42e-491a-8bf2-7b5a1e592e0b" />

**rsync**
This is basically used to make synchronous changes or file transfer. we will be using WSL and CentOS to link and transfer file as on WIndows we dont have builtin rsync.
<img width="1556" height="397" alt="image" src="https://github.com/user-attachments/assets/ff83c907-4ea3-4c3c-8a40-763015e6bb52" />


# 24 Dec 2025

## top, CPU stats, RAM, clean buffer cache, IoStat
### top 
top command is used to check the processes running and cpu processes and resources being used.
### CPU stats
when we run the top command cpu stats shows us the CPU status broken down in us (user) , sy (system) , id (idle) <br>
<img width="1249" height="325" alt="image" src="https://github.com/user-attachments/assets/92311166-e2ed-4377-9ce9-1eb89cfc0159" />

### clean buffer cache 
this is used to clean the buffer cache as sometimes processes use the available buffer cache space to optimize the performance. <br>
to check the memory in human readable form we use free -h 
<img width="1140" height="119" alt="image" src="https://github.com/user-attachments/assets/81d3b2c3-c017-4e58-8fc7-1764349a465c" />

To clean cache we have the following commands <br>
**Clear PageCache**: sync; echo 1 > /proc/sys/vm/drop_caches <br>

**Clear Dentries and Inodes:** sync; echo 2 > /proc/sys/vm/drop_caches <br>

**Clear All (PageCache, Dentries, Inodes):** sync; echo 3 > /proc/sys/vm/drop_caches <br>






# 26 Dec 2025

## Installing nginx 
To install nginx we need to run the followig commands<br>
yum update<br>
yum install nginx<br>

## Service management (Start,Stop,Restart,Enable,Status) <br>
### Start
this is used to start the nginx service. Its command is <br>
service nginx start
### Stop 
THis is used to stop the nginx service . iTs command is <br>
service stop nginx <br>
### Restart
this is used to restart the nginx service. Its command is <br>
service nginx restart
### Enable 
This is used to Enable the nginx after starting. its command is <br>
service nginx Enable
### Status 
This is used to check the status of the nginx . Its command is <br>
service nginx status

## Nginx Configuration Management	Main config files & directory

This is where main configuration of nginx is being rendered<br>
Main configuration is present in /etc/nginx/nginx.conf <br>
here we can manage ports and location of the nginx <br>

## Nginx Reverse Proxy Setup - Nginx Port & Firewall Configuration	Setup reverse proxy for a web app

This is used to let nginx frontend server to reach to the backend server instead of the default static files listed in /usr/share/nginx/html.<br>
for this we have to add location parameter instead of root in /etc/nginx/nginx.conf
<br>
Also to add the port forwading rules 8181 of host to 81 of guest(internal).<br>
also we have to add extra port to firewall using command firewall-cmd --permanent addport=tcp/81 <br> and then restarting the firewall
using the command firewall-cmd  --reload

<img width="941" height="356" alt="image" src="https://github.com/user-attachments/assets/85ebe396-7c1f-4583-996c-7d2e23d56e7a" />
<img width="1211" height="414" alt="image" src="https://github.com/user-attachments/assets/5e0a48e0-6f3b-4e1d-9b2f-08c924c040a1" />
<img width="1424" height="226" alt="image" src="https://github.com/user-attachments/assets/c96f41a7-cc5c-4b83-9105-435883d61e53" />
## Nginx Networking - Nginx Logs	Configure multiple server blocks	


### Configure multiple server blocks	
This is used to create multiple server blocks. for this we have to define different servers and their configurations in /etc/nginx/nginx.conf file. 

### Nginx logs
these are located in /var/log/nginx and are access.logs and error.log


# 29 Dec 2025 

## Installation & Setup	Install Apache on centos

To Install Apache on Centos we have to run the following commands <br>
**yum/dnf update** <br>
**yum/dnf install httpd**  this is so because in centos dnf is the new package manager and is replacing the yum . Also in CentOS apache is known as httpd.<br>
Practical work is as follows.

<img width="1179" height="150" alt="image" src="https://github.com/user-attachments/assets/68ec6e41-8685-4256-aa14-1c5637d4bdb2" />

<img width="1344" height="177" alt="image" src="https://github.com/user-attachments/assets/e8037d28-1cda-4367-9b17-93e17f72f154" />



##  Apache Service Management	Start,Stop,Restart,Enable,Status

### Status 
After Installation we need to check the status of the apache server. for that purpose we need to run the following command .
<img width="1308" height="163" alt="image" src="https://github.com/user-attachments/assets/effbc62d-345a-4fb8-8f73-bdbeeb22d7ad" />


### Start 
To start the service if it is stopped or first time installed we need to run the following command .
**service httpd start**

<img width="787" height="47" alt="image" src="https://github.com/user-attachments/assets/52c6e188-2acb-42fe-a9b3-065f393d51f7" />
<img width="1473" height="220" alt="image" src="https://github.com/user-attachments/assets/9e541523-1fc2-4ebc-a77b-39bb7a34f5e3" />




### Enable
This command is used to enable the service for fututre as well so that when restart our OS it starts automatically as start only do it for the current work only. Also we need to use systemctl as service is old now and doesnot work.
<img width="1283" height="65" alt="image" src="https://github.com/user-attachments/assets/0435a59d-e38a-447f-b6e1-3e8ce9dff753" />


### Stop 
this is used to stop the running service so we may make changes or free up the resources when not in use.
<img width="1916" height="371" alt="image" src="https://github.com/user-attachments/assets/50eab06f-b463-4d5d-b542-286a030eb219" />


### Restart 
THis is usally used when we make some changes in the service configuration so inorder to implement them completely we need to run this command . 
<img width="813" height="41" alt="image" src="https://github.com/user-attachments/assets/dcc801f0-0eb0-4988-9dbf-e938561486cc" />


## Configuration Management	Create and manage Virtual Hosts

For this purpose we have to add the port in the /etc/httpd/conf/httpd.conf file . if port is allowed by selinux then ok otherwise run the command <br>
**semanage port -l | grep http_port_t**  to check . If not available then run the command <br>
**semanage port -a -t http_port_t -p tcp <portNO>**. <br>
This will add the port. <br>
Now run the command <br>
**firewall-cmd --add-port=8082/tcp --permanent** <br>
After this run the command <br>
**firewall-cmd --reload**  <br>  

As we are running on virtual box so we have to add the port forwarding rules here <br>
After that we just have to run the command <br>
**systemctl restart httpd**  and our server will be running and can be accessed on host localhost port.

And for the purpose of running multiple ports we have to <br>

Define Listen <port> in httpd.conf in conf . 
Add the virtual host files like 
<img width="928" height="220" alt="image" src="https://github.com/user-attachments/assets/e9cd7656-7e8f-468b-a84b-3b31c61013e0" />

and then create the site files in /var/www/sitefolder/files.<br>
After this we have to follow the exact same rules to add the port and then restart the systemctl and we will be able to run the servers.   








































































  











