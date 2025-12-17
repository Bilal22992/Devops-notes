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










