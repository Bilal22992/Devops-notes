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


