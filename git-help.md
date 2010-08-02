---
title: Git Help
layout: default
---

Git Barriers
------------

This page will be used to collect some common barriers when first entering git.

### Committing

Recommended way to commit is:
    
    git commit -am "comment saying what was done"

The <code>-a</code> flag includes all changes that are staged (you can see this via <code>git status</code>). However, it does not include any new files that haven't been added yet (which you can do by <code>git add .</code> which adds all new files, or <code>git add file-name</code> to add individually).

The <code>-m</code> flag lets you attach a one line comment. Every git commit needs a comment. If you don't used the m flag, git will open up vi. You can quit vi by typing <code>:q</code>
