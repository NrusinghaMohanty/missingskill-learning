# Introduction of Linux #

## What is Linux ? 

* First of all I have to clear that Linux is not an operating system like other popular operating systems . It is actually a Linux kernel. Different distributions of Linux makes it comparable to other OS.
* Linux is an operating system or a kernel distributed under an open-source licens.
* Various companies or entities can make their own version of OS using Linux kernel.
* Some popular distribution names are
  - Debian
    - Ubuntu
  - Redhat
    - Fedora
    - centOS
    - Mint  

## History ##

In 1970 a company called bell lab created a common software for all computer and named it as "unix" . Initially, Unix was only found in large organizations like government, university, or larger financial corporations because it was expensive at that time for common people. Then in 1983, Richard Stallman developed GNU project with the goal to make it freely available Unix like operating system and to be used by everyone. But this project failed to gain popularity . Then 1991 a student name Linus Torvolds created a software to interact with system and name it as kernel. Later on Richard stallman and Linus Torvolds came together and created the first Linux based operating system known as GNU Linux.

# Basic commands in Linux #

Linux provides a CLI (Command Line Interface) to communicate with the OS. Here are the most basic of the Linux Commands

### 1. CD

 CD command stands for "change directory". With the cd command, you can change your current working directory.

 Syntax :-
- ` $ cd directory_name `

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
 |  ls -l | Display all the file details in list format |
 |  ls -h | Display all the file details in human readable list format |
 |  ls -t | Shows all the file in asending order of its creation(new file on top & old file on bottom) |
 |  ls -r | Show all the file in decending order of its creation(old file on top & new file on bottom) |
 |  ls -F | To catagorie which file is directory(it add a / in the end if it is a directory) |


### 5. TOUCH

 touch command is used to create empty files and also changes the timestamps of existing files on Linux System. Changing timestamps here means updating the access and modification time of files and directories.

 Syntax :-
- ` $ touch new_directoryname `

### 6. MKDIR

 mkdir stands for "make directory". mkdir command in Linux allows users to create or make new directories in current working directory.

 Syntax :-
-  ` $ mkdir directory_name `

### 7. HELP
 
 help command used for summary of a particular command and its flag.

 Syntax :-
- ` $ command_name --help `

### 8. MAN

 man command stands for "manual".It shows all the flag of a particular command in detail way.

 Syntax :-
- ` $ man command_name `

