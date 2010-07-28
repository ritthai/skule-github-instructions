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

Make sure you config your git afterwards:

    git config --global user.name "Your Name"
    git config --global user.email "email.you.signed.up.to.github.with@example.com"

Now, there are two ways to develop: being a casual developer or a project developer.

3) Be a Casual Developer
-------------------------

The key difference between a casual developer and project developer is that a project developer access to the production server. 
As a casual developer, you can dive right in and make fixes... but a project developer will have to check them before they get accepted.

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

### 4.a) Clone the Repo

Once you have confirmation from rafd, you can get a local copy of the repo:

    git clone git@github.com:ProjectName.git

Now you can pull, push, etc. to the skule repo.

### 4.b) Get Access to Production Server

In order to authenticate with the production server, you'll need to [email the sysadmin](mailto:sysadmin@skule.ca) 
or message rafd your public key (the .pub file you created when setting up your github account).

Once you have confirmation, add the production server repo by running the following: (remember the change ProjectName)

    git remote add web git@srv.skule.ca:ProjectName.git

### 4.c) Develop

You should be doing all testing, etc. locally. Frequently push to origin (GitHub) to keep others in the loop, to do so, just run:

    git push origin master

When you're ready to push to the production server (ie. make it live on \*.skule.ca), just run:

    git push web master

...and like magic, it's live!