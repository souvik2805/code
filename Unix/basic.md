## Topic - 1

### Components of UNIX:
 - Shell
 - Kernel
 
#### 1.Shell
It is the outer layer of UNIX Operation system.
Shell reads command provided by user.
Shell will check is it valid command or not.
If everything is proper, then shell interprets/converts the command into kernel understandable form and handover that to the kernel.
Shell acts as interface between user and Kernel.

#### 2. Kernel
It is the core component of UNIX Operating system.
It is responsible to execute our commands with the help of hardware components.
Memory allocation and processor allocation will takes care by kernel.
It acts as interface between shell and hardware components.


#### Command Execution Flow:
normal user ==> $ prompt
super user/root user/admin user ===> # prompt
sudo -i ===> To switch to superuser

#### The most Commmonly used basic commands : 
1. pwd --> print working directory
2. ls --> list out all files and directories
3. mkdir --> To Create/make a directory
4. cd --> Change directory
5. touch -->To create an empty file
6. rmdir --> To remove a file
7. rm --> To remove  a file
8. cal ==> Display Current Month Calander
9. date ==> Display Current date and time
10. help ==> To display list of available commands
11. clear ==> To Clear the Terminal 
12. exit ==> To logout session
13. hello => To display brief system information
-----------------------------------------------------
User home directory for durga : /home/durga
User home directory for ravi : /home/ravi


## Topic 2. Linux File System
 
#### Types of files in linux

In python everything is treated as Object
In Linux everything is treated as a file

1. Normal files or ordinary files (images, video, docs...)
2. Directory Files
3. Device Files

 - In Linux file extension is not important. Based on our content the linux can identify file type.
 
terminal 1 ===> /dev/pts/0
terminal 2 ===> /dev/pts/1
[send coammand one terminal to other by >]
[Expample : echo "I ..." >dev/pts/1]

Note: 
ctrl + alt + t ==>To Open terminal 
ctrl + d ==> TO Close the terminal


##### File Type  :
 -> ls -l 
The first character represent the type of the file
d---> Directory file
```-```  ===> Ordinary File
l ====> Link File


c ====> Character Specila File
b ====> block special file
s =====> Socket File

## Topic 3. File System Navigation Commands : 

 - Hidden files and hidden directories
```
ls
ls -a
```
-a means all

```. ```  ===> present directory
```..```  ===> represent parenet directory

root == /

1. $ cd ````. ````
        Change to Current directory(Uselesss)
2. $ cd ``` ..```
        Changes to parent directory

3. $ cd  ```~```
        To go to user home directory 
        /home/durga

4. $ cd 
        cd command without any argument
        To go to user home directory 
        /home/durga

5. $ cd ```-```
        If we want to go previous working directory.

#### Linux File System Hierarchy: 

Linux system has tree like structure
It start with root (/)
/ is the topmost directory
 - Subdirectory:
 ```
 bin etc home lib dev usr cdrom
 ```
 
 1. bin directory:
------------------------
bin means binary.
It contains all binary executables realted to our linux commmands.
```
touch
ls
mkdir
cd 
```

2. sbin directory
--------------------
sbin means systembin.

normal user used commands related binary executable files availble in bin directory.
super user used command related executalb  files avaiable in sbin dirctory.
```
Disk pratitioning
network mangement
```

3. etc directory
------------------
This directrory contains all system configuration files.
These configuration files can be used by operation system it self.

/etc/passwd ===> All user information
/etc/group ===> All group information
/etc/hosts ===> All hosts information( ip address and dns name)
