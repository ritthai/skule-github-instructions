---
title: Trusted Development
layout: default
---

Be a Trusted Developer
---------------------

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