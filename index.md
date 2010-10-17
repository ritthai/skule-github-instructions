---
title: Home
layout: default
---

So, you're interested in contributing to Skule code? Awesome! Here's how to get started... 


0) Pick a Project
-----------------
A list of projects is available on the [skule github page](http://github.com/skule/).


1) Install Git
--------------

What's git? It's the most awesome [version control system](http://en.wikipedia.org/wiki/Revision_control) ever. 
If you don't have git installed, head on over to [here](http://git-scm.com/download) and grab one of the binaries. 
(If you're on Windows choose the Cygwin version)

Never used Git or a version control system before? 
Give [GitRef](http://gitref.org/) and/or [Git for the Lazy](http://www.spheredev.org/wiki/Git_for_the_lazy) a read.


2) Create a GitHub Account
--------------------------

Head on over to [GitHub](http://github.com/) and create an account.

As part of the account creation process you will need to generate an RSA key-pair. Giving GitHub your public key means GitHub can validate that you are the correct user because only you have the corresponding private key and password.

Make sure you config your git afterwards (without the quotes):

    git config --global user.name "username"
    git config --global user.email "email.you.signed.up.to.github.with@example.com"

You can confirm that your configuration has changed using:

    git config --get user.name
    git config --get user.email

Now, there are two ways to develop: being a casual developer or a project developer.

3) Choose Your Style
--------------------
There are two ways to contribute: being a [casual developer](casual-development.html) or a [trusted developer](trusted-development.html). Both will let you contribute code: it's mostly a question of commitment and trust.

As a [casual developer](casual-development.html), you can dive right in and make fixes... but a trusted developer will have to check them before they get accepted.

[Trusted developers](trusted-development.html) have direct access to the skule github repo, and can also deploy to the production server.

### 3.a) Fork the Repo

Go to the github project page for the project you want to work on and "fork" the project.
This will create a personal version of the project for you.

### 3.b) Clone the Repo

On your computer, run:

    git clone git@github.com:YourUser/ProjectName.git
    
### 3.c) Make Changes

### 3.d) Commit, Push and Pull Request

4) Be a Project Developer
-------------------------

Instead of having to make pull requests, project developers have direct access to the skule repo. 
To get access, message [rafd](http://github.com/rafd) and include which projects you're interested in.
Project developers can also deploy to the production server (see below).

### 4.a) Clone the Repo

Once you have confirmation from rafd, you can get a local copy of the repo:

    git clone git@github.com:username/ProjectName.git

Example:

    git clone git@github.com:skule/SkuleTheme

Now you can pull, push, etc. to the skule repo.

### 4.b) Get Access to Production Server

In order to authenticate with the production server, you'll need to [email the sysadmin](mailto:sysadmin@skule.ca) 
or [message rafd](http://github.com/rafd) with your public key (the .pub file you created when setting up your github account).

Once you have confirmation, add the production server repo.

First, use cd to change to the correct directory.

    cd ProjectName

Example:

    cd SkuleTheme

Then run the following: (remember to change ProjectName)

    git remote add web git@srv.skule.ca:ProjectName.git

### 4.c) Develop

You should be doing all testing, etc. locally. Read step 5 for more details about developing locally.


Frequently push to origin (GitHub) to keep others in the loop, to do so, just run:

    git push origin master

### 4.d) Deploy

When you're ready to push to the production server (ie. make it live on \*.skule.ca), just run:

    git push web master

...and like magic, it's live!


5) Recommended Git Workflow
-------------------------

### 5.a)

for everyone new feature/bug fix, create and checkout a branch 
first use change to the project directory
then
    
    git checkout -b dev-branch-name

### 5.b)

work on said feature in the branch until complete and tested, commit often 

    git add file-to-add

    git commit -am "comment about this commit"

### 5.c)

update dev branch from master when needed

    git pull origin master

    git merge master

### 5.d)

when complete, switch to master, merge in your dev branch

    git checkout master

    git merge dev-branch-name

### 5.e)

delete dev branch if needed 

    git branch -d dev-branch-name

### 5.f)

push to development repo

    git push origin master

### 5.g)

push to web

    git push web master
