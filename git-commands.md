# Setup & Config
- set up your git 
- `git config --global user.name "your username"`
- `git config --global user.email "your useremail"`
---
## `git config --list`
- It will show you the detail of your configuration

----
## `git init`
- It initialize your new repository in your local machine.

---
## `git status`
- It will show you status of stages of your files

---
# Basic Workflow
## `git init`
- It initializes a new Git repository.

## `git status`
- It shows working directory status.


## `git add <yourfile>`
- It add and Stages changes for commit.

## `git commit -m " your ref. message "`
- It records staged changes.


---

# Viewing Changes

## `git log`
- It shows commit history.

## `git log --oneline`
- It show commit history in summaries form in oneline

## `git diff`
- It shows changes not yet staged.

## `git restore`
- It restores files in working directory.

## `git add .`
- It stages all changes in current directory.

## `git branch <your branch>`
- Lists branches.

## `git checkout`
- It switches branches.

## `git remote add origin https://github.com/sumit9165/devops-git-practice.git`
- It will add your local repository to remote repo

## `git push -u origin <your local branch>`
- It will push your local branch to remote with all commits of this branch.
- you can push your all branches to remote.


---
## What is the difference between origin and upstream?
- You clone from upstream to create origin (your fork),
- then use upstream to pull updates and origin to push your contributions
- origin = url of your remote repository, where you have pull/push access.  
- upstream = your forked repository's origin
-----
## What is the difference between git fetch and git pull?
-  Fetch Changes from Upstream: `git fetch upstream`
-  To keep your local repository up-to-date with the original repository, fetch the latest changes:
-  Push Changes to Origin: `git push origin main`
-  After merging the changes from the upstream repository, push your updated `main` branch to your forked repository on GitHub:
------------


