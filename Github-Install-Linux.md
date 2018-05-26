This tutorial was taken from https://wiki.paparazziuav.org/wiki/Github_manual_for_Ubuntu#How_to_use_Github

# Github manual for Ubuntu

## Introduction to Github
Developers often use a version control system for developing their software projects. 
A version control system allows the creation for a collection of files (such as a software project). The user also has the opportunity to switch back to an older version of the collection.

GitHub (git) is a distributed version control system (dvcs), it doesn't have a central server but every local copy contains the full history of the collection. GitHib is open source, for more information about repository's and Github, please visit Wiki GitHub. If you do not have a GitHub account and you would like to contribute to a project or develop a project on your own, please register at github.com and follow their "Bootcamp".

This manual works only for ubuntu users! 

## Github and Ubuntu
Github doesn't provide an easy step-by-step guide for using your repository with ubuntu, if you need (or would like) to use ubuntu and github together, we provide a nice and easy guide. This page will help you to Setup github for Ubuntu and use Github. At the end there will be a small summary or so called: "Cheatsheet" with the command's you might need.

## Setup Github
When you have a github-account, you may install Github. Before installing Github, you need to set up the ssh keys. This manual will also guide you trough cloning and configurnig with github.

### Setup the SSH-key
Open the terminal in Ubuntu.
Type: 

`$cd ~/.ssh` 

When the terminal displays: ""bash: cd: ./.ssh:No such file or directory" you should generate a public/private rsa ket pair, continue with step 3. 
If the terminal changes to ~/.ssh directory, continue with step 5.
Open a new terminal and type: 

$ ssh-keygen -t rsa -C "your_email@youremail.com" 

After hitting Enter, the terminal will say: 'Generating public/private rsa ket pair. Enter file in which to save the key(/Home/ubuntu/.ssh/id_rsa):' please press only enter and the terminal will ask to enter a passphrase.
Enter a suitable passphrase which is > 4 characters. If this is done, please continue with step 6.
(Follow this step only if your terminal changed to "~/.ssh") 
You already have some SSH-keys, following commands will backup (in folder "key_backup") and remove the keys. Type in your terminal: 

$ mkdir key_backup 
$ cd id_rsa* key backup 
$ rm id_rsa* 

Add the SSH-key to github, type in the terminal: 

$ gedit id_rsa.pub 

Ubuntu will open a file, copy it's entire content:
Open the github site and login.
Go to "Account Settings" (in the upper right corner from your page).
Click: "SSH Keys"
Click: "Add another public key"
Paste the copied content into the "key field" and press "Add key" 

Open the terminal again and type the following command: 

ssh-add 

This is only required if you use ubuntu (which all the readers of this document should, as described in the introduction.)
Your setup for the ssh-key is completed! Now you are ready to install github.

## Install Github
Open the terminal and type the following command: 

$ sudo apt-get install git-core git-gui git-doc 

Your terminal will download some things and install github automaticly. When it's done, your installation is complete! The next step is getting your local copy of the repository (or code-branch), follow the instructions for "Cloning".

## Cloning
Cloning is a way of downloading a local copy of your project. The following command will clone the code branch, just replace "username" with you GitHub username and project name with the name of project on github: 

$ git clone git@github.com:username/projectname.git

Be aware, do not misspell the command, it won't work. If you are having trouble, read the given error and try to solve him by reading the following page: GitHub help.

## How to use Github
When you have a local copy of your project on your system, you can edit the files (if you have the correct permission). It is important to keep your copy up to date, so all the collections on all the systems are the same. To do so you'll need to understand the following: pulling the newest version from the repository, Adding files to the repository, commit the changes. These are the most important subject for using the repository. We will also discuss some other very usefull commands.
