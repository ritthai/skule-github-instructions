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
If you don't have git installed, had on over to [here](http://git-scm.com/download) and grab one of the binaries. 
(If you're on Windows choose the Cygwin version)

Never used Git or a version control system before? 
Give [GitRef](http://gitref.org/) and/or [Git for the Lazy](http://www.spheredev.org/wiki/Git_for_the_lazy) a read.


2) Create a GitHub Account
--------------------------

Head on over to [GitHub](http://github.com/) and create an account.

Make sure you config your git afterwards:

    git config --global user.name "Your Name"
    git config --global user.email "email.you.signed.up.to.github.with@example.com"

Message [rafd](http://github.com/rafd) so that he can include you in the Skule developers group
(and include which projects you're interested in). Alternatively, you can develop the 'github way.' (see below)


3) Clone the Repo
-----------------

Once you have confirmation from rafd, you can get a local copy of the repo:

    git clone git@github.com:ProjectName.git


4) Send Over Your Public Key
-----------------------------

In order to authenticate with the production server, you'll need to [email the sysadmin](mailto:sysadmin@skule.ca) 
or message rafd your public key (the .pub file you created when setting up your github account).


5) Add the Production Server
----------------------------

Once you have confirmation, just run the following: (remember the change ProjectName)

    git remote add web git@srv.skule.ca:ProjectName.git


6) Develop
----------

You should be doing all testing, etc. locally. Frequently push to origin (GitHub) to keep others in the loop, to do so, just run:

    git push origin master

When you're ready to push to the production server (ie. make it live on *.skule.ca), just run:

    git push web master

...and like magic, it's live!



The GitHub Way
--------------

Instead of joining [the Skule github group](http://github.com/skule), you can contribute by: forking the repo, making your own changes, and then making a pull request (and we'll push to production).

