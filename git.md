# Introduction 

## what is git ?

* Git is an an open-source distributed version control system for tracking changes in computer files.
* So What is version control system ? it is a system that provides with you the features of keeping a record of your software code changes, who made those changes, and at what time in a repository/folder. it just like a snapshot of every changes you have made in a code.

## Feature of Git

* If you accidentally change your code and break something, git can revert it.
* If you accidentally delete your code, using git can help you get it back.
* Sharing your code or work with other developers on the same project.
* It tracks the changes while someone makes changes in a file with a commit message.
* By help of this we can deploys the source code on the remote server.
* Experimenting with your code without messing with the production version.

## Git three stages

Git has three stages :-

1. Modified - modified means that you have made changes to the file but have not committed it to your database yet.
2. Staged - staged means that you have added the modified file in its current version to go into your next commit snapshot.
3. Commited - committed means that the data is stored in your local git database.

## Centralized version control system

* As we now know, Git mainly works locally. Now you can ask, you said earlier that multiple developers can work together on a single project, but how can multiple developers work together on a local project. So here centalized version control system come to picture. It is a place that provides you with repository(a place where we store our software project) hosting service on the cloud.

* Some of popular centralized version control system,
  * Github
  * Gitlab
  * Bitbuket

# Git command

| Command | Explanation |
| ------- | ----------- |
| git config --global user.name "user_name" | To setup your username associated with git commit globally |
| git config --global user.email "email_address" | To setup your e-mail id associated with git commit globally |
| git config --list | To how the user name and e-mail id both |
| git status | it will show you information about the current state of your files in a git repo, and highlight any differences from the last time you used 'git commit' |
| git init | To make existing folder/file into a git repo |
| git add --a / git add . | To add all the file into staging area |
| git add file_name | To add a particular file into staging area |
| git commit -m "commit message you want to write" | To make a file snapshot/record |
| git commit -a -m "commit message you want to write" | To add the staging area and commit simuntously |
| git checkout commit "commit message" | To go to that commit |
| git checkout -f | To check all the file to previous commit |
| git diff | To show the differnece between working directory with staging area |
| git log | To show all the commit which have done in a file or code |


## Brancing 

* This is probably the most basic use case of a version control system. When you have an app running in production, typically you would not want to change its code as it might impact your live app. So, if you want to make any changes, first you need to create a copy of the original repo, and then work on it. Git allows us to easily create this copy by using Branches. The original repo is usually called the main branch or master branch. The copied branch can be named anything, feature, beta, v1.0, v2, depending on the naming scheme of your team.

| Command | Explanation |
| ------- | ----------- |
| git branch | To show all the branch |
| git branch branch_name | To create or make a branch |
| git checkout branch_name | To switch or go to given branch |
| git checkout -b branch_name | To make a branch and switch to that directly |
| git merge branch_name | To merge given branch to your own branch |
| git branch branch_name -d | To delete a branch | 

## Cloning

* It's not a good idea to keep your code only in your local machine. If something happens to your computer, you will lose all your code. To prevent this from happening, we normally host our repos in servers like Github, Bitbucket, Codecommit, etc (Github being the most popular one). If your fellow developer wants to work on the code, they will need to download a copy of your code into their local machine. This process of downloading the code into our local machine from a server is called cloning.

| Command | Explanation |
| ------- | ----------- |
| git clone clongefile_http | To clone a file/code |

## Pull
* In a team, there will be more than one developer working on the code. The code in the server constantly keeps getting updated. But these changes will not be automatically downloaded into your local machine. To get the code into your local machine you need to pull. Pull will get the latest code of your selected branch into your local machine. 
