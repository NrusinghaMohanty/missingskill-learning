# Introduction of Linux #

## What is Linux ? 

* First of all I have to clear that Linux is not an operating system like other popular operating systems . It is actually a Linux kernel. Different distributions of Linux makes it comparable to other OS.
* Linux is an operating system or a kernel distributed under an open-source license.
* Kernel is the core component of the operating system. It nothing but a lowable software which interact with hardware.  
* Various companies or entities can make their own version of OS using Linux kernel.

## History ##

* In 1970 a company called bell lab created a common software for all computer and named it as "unix" . Initially, Unix was only found in large organizations like government, university, or larger financial corporations because it was expensive at that time for common people. Then in 1983, Richard Stallman developed GNU project with the goal to make UNIX like OS freely available and to be used by everyone. But this project failed to gain popularity . Then 1991 a student name Linus Torvolds created a software to interact with system and name it as kernel. Later on Richard stallman and Linus Torvolds came together and created the first Linux based operating system known as GNU Linux.
* Some popular distribution names are
  - Debian
    - Ubuntu (based on Debian)
      - Mint (based on Ubuntu)
  - Redhat
    - Fedora(based on Redhat)
    - centOS (based on Redhat)

# Basic commands in Linux #

Linux provides a CLI (Command Line Interface) to communicate with the OS. Here are the most basic of the Linux Commands :-

### 1. CD

 CD command stands for "change directory". With the cd command, you can change your current working directory.

 Syntax :-
- ` $ cd directory_name `

 other variant 

 | command | Explanation |
 | ------- | ----------- |
 | $ cd    | it takes user to its home directory |
 | $ cd -  | it takes user the previous folder where user work in other words its hold the last position |
 | $ cd .. | it takes user to one step back or previous folder |
 | $ cd ../file_name | it takes user one step back and look for the file name given and take user into it|
 
 ### 2. WHO & WHOAMI

 who command lets you display the users currently logged in to your Linux operating system in the terminal/shell. To know about how many users are using or are logged-in into a particular Linux-based operating system, user can use the "who" command to get that information.

 Syntax :-
- ` $ who `

 whoami command is used to print the user's name from which they are currently logged-in. In other words, it displays the name of the currently logged-in user in the terminal/shell.

 Syntax :-
- ` $ whoami `

### 3. PWD

 pwd command stands for "print working directory" and will show you the name of your current working directory – that means “where you are” right now.

 Syntax :-
- ` $ pwd `

### 4. LS

 ls stands for "list". It is used show the list of directory/folder in current working directory/folder.

 Syntax :-
- ` $ ls ` 

 | Command | Explanation |
 | ------- | ----------- |
 |  $ ls -l | Display all the file details in list format |
 |  $ ls -h | Convet and display all the file details in human readable list format |
 |  $ ls -t | Shows all the file in asending order of its creation(new file on top & old file on bottom) |
 |  $ ls -r | Show all the file in decending order of its creation(old file on top & new file on bottom) |
 |  $ ls -F | To catagorie which file is directory(it add a / in the end if it is a directory) |
 |  $ ls -a | To show the hidden folder or file(any directory or file start with . is hidden directory or file) |


### 5. TOUCH

 touch command is used to create empty files and also changes the timestamps of existing files on Linux System. Changing timestamps here means updating the access and modification time of files and directories.

 Syntax :-
- ` $ touch new_filename `
 

### 6. MKDIR

 mkdir stands for "make directory". mkdir command in Linux allows users to create or make new directories in current working directory.

 Syntax :-
-  ` $ mkdir directory_name `

 To create a sub-directory under a directory we can use below command

- ` $ mkdir directory1/directory2 -p ` (Here directory2 is created under directory1)

 To create a multiple directory we can ue below  command,

- ` $ mkdir directory1 directory2 directory3 `

### 7. HELP
 
 help command used for summary of a particular command and its flag.

 Syntax :-
- ` $ command_name --help `

### 8. MAN

 man command stands for "manual".It shows all the flag of a particular command in detail way.

 Syntax :-
- ` $ man command_name `

### 9. CLEAR

 clear command used for clean the terminal/shell screen.

 Syntax :-
- ` $ clear `

### 10. CAT

| Command | Explanation |
| ------- | ----------- |
| $ cat file_name | Display or read contents of file on terminal |
| $ cat > file_name | It i use to create new file/It also overwrite the existing file content |
| $ cat >> file_name | It update or modifying the existing file content |

### 11. RM & RMDIR

 rm command stand for "remove". It is used to delete the specifie file where rmdir command stands for "remove directory". It delete only the empty directory.

 Syntax :-
- ` $ rm directory_name ` 
- ` $ rmdir directory_name `
 
 To delete a directory and its sub-directory or folder we can use below command,

 Syntax :-
- ` $ rm -rf directory-name `
- ` $ rm * ` ( it delete all the files in a directory/folder)
- ` $ rm -rf * ` ( it delete all the directories/folders in a directory/folder)
- ` $ rm directory_name/file_name ` ( it delete the file_name inside the directory_name)
- ` $ rm -rf directory_name1/directory_name2 ` ( it delete the directory_name2 inside the directory_name1)

### 12. MV & RENAME

 mv command stand for "move". mv is used to move one or more files/directories from one place to another.

 Syntax :-
- ` $ mv file_name folder_name ` ( Here file_name moves to the folder_name )
- ` $ mv folder_name2 folder_name1 ` ( Here folder_name2 moves to the folder_name1 )

if we want to rename the file or directory/folder we can use below command,

 Syntax :-
- ` $ mv old_filename new_filename `
- ` $ mv old_foldername new_foldername `

### 13. CP

 cp command stands for "copy". cp is used to copy one file or folder/directory from one place to another .

 Syntax :-
- ` $ cp copy_filename destination_foldername `
- ` $ cp -rf copy_foldername destination_foldername ` ( for folder/directory) 

### 14. HISTORY

 history command is used to view the previously executed command in the terminal/shell . These commands are saved in a history file.

 Syntax :- 
- ` $ history `

### 15. ECHO

 echo command is just printi/display specified text given by user in ther terminal/shell . it is mostly used for print the system path where user is working.

 Syntax :-
- ` $ echo Whatever_user_want_to_write `
- ` $ echo $PATH ` ( To see system path where user is working)

### 16. WHICH

 In linux everything is file and all s/w are command. By "which" command we can show the path of a particular command given.

 Syntax :-
- ` $ which command_name `

### 17. WGET
 
 wget command basically used to download or fetch the html file of a particular website.

 Syntax :-
- ` $ wget website_name `

### 18. LESS AND MORE

 less command shows o/p in a pagewise manner. it basically used to show larger text file in the terminal/shell.( we can see next page us using "spacebar_key", "w_key" for previous page, "q_key" for exit).more command is as less command the main difference between more and less command is that less command is faster because it does not load the entire file at once but more comand do.

 Syntax :-
- ` $ less file_name `
- ` $ more file_name `

### 19. TOP AND PS

 top command stands for "table of process". it allows users to monitor processes, CPU information and memory utilization, where ps command allows users to show all current running application in the terminal.

 Syntax :-
- ` $ top `
- ` $ ps `

### 20. PING

 ping comman used for verifying connectivity between two hosts on a network.It confirm that a remote host/server is online,responding and its possible speed.

 Syntax :-
- ` $ ping server_name `

### 21. SSH

 ssh command used to access to a host/server remotely.

 Syntax :-
- ` $ ssh server_name `

### 22. IFCONFIG

 By using ifconfig command user can configure IP Addresses in Linux. 

 Syntax :-
- ` $ ifconfig `
- ` $ ipconfig ` (for window)


# File system 


* Everyting in linux is a file even if it is a folder,program,memory or anythingelse. and everything starts with a root directory and root directory starts with "/" and evrthing comes under this.
* "/" indicate the root file sydtem.
* If we want to goto ytem root directory we can execute command like below,

    ` $ cd 
      $ cd / ` 


## ALL NECESSARY FILE AND EXPLANATION

| File | Explanation |
| ---- | ----------- |
| /boot | Here kernel configuration or aplication is stored/located |
| /root | It is the home folder for root user(system admin) |
| /grub | It is boot loader. it is where pickup the location of kernel |
| /bin | All the binary files or commands that we used is stored | 
| /sbin | System binary(which is comes with kernel), used by system admin |
| /home | It is user home folder in other word all the user data stored here |
| /var | System level variable(log file) stored here |
| /usr | User system resource. Here user related s/w are stored |
| /tmp | It is used when system want something stored temporarily |
| /etc | Here system configuration or s/w are stored |
| /lib | System libaries are stored here |
| /dev | External devices are mounted here(ex. usb,mouse,keyboard etc) | 
| /proc | System level process or information is shown( it not a folder,it is a in memory file) |
| /opt | s/w related files or data stored here |