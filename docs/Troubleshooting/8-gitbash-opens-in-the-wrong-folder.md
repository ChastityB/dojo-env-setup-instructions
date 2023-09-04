---
layout: page
title: GitBash Opens in the Wrong Folder
parent: Troubleshooting
nav_order: 8
---

# GitBash Opens in the Wrong Folder

## PROBLEM:

Opening GitBash from Windows start menu (not from Github Desktop) and starting jupyter notebook displays a folder containing bin/cmd/dev/etc ( see screenshot below) instead of the expected User folder with Documents/Downloads/etc.

![](../../images/lp/gitbash_wrong_home.png)

## Cause

Your GitBash program defaults to the folder where GItBash is installed. What you are seeing above is the contents of C:/Program Files/GitBash. This happens to a small percentage of windows users.

### Solution/Workaround

- First, run the following echo command to add one more alias to GitBash and then open a new GitBash window

`echo 'alias ~="$HOME"' >> ~/.bash_profile`

- Now test the command by runing the commands below to change directory to "~" and to display the current folder name.

`cd ~ ls`

- If you can see your Downloads, Desktop, Documents, etc. folders then the alias worked!

### New Workflow

- From now on, if you want to open a GitBash in your user folder, you will run "cd ~" as soon as you open a new GitBash window.
  - Note: if you are opening a specific repo from GitHub Desktop you will NOT want to run this command, since you are already in the desired folder.
