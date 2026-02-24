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

## `git branch`
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

---------
## What is the difference between clone and fork?
- Fork (Server-side): Creates a copy of a repository in your GitHub/Bitbucket account. It acts as a separate, independent repository that you own.
- Clone (Local-side): Downloads an existing repository from a remote server (GitHub) to your local computer. It creates a local copy, including all history and branches.
-------
## When would you clone vs fork?
Fork when:
- You want to contribute to someone else's project (Open Source).
- You want to use another project as a starting point for your own, but keep it separate.
- You do not have write access to the original repository.
Clone when:
- You have permission to push changes directly to the repository.
- You are starting work on a local machine after forking a project.
- You just want a local copy of a project to read, test, or run, without intending to push changes back.
------
## After forking, how do you keep your fork in sync with the original repo?
1. GitHub provides a built-in "Sync fork" feature that allows you to update your fork with a few clicks.
2. Command Line Interface.
To sync from your terminal, you must first configure a remote that points to the original repository.
- `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git`
- Fetch the latest changes: `git fetch upstream`
3. GitHub CLI
If you have the GitHub CLI installed, you can sync your fork with a single command:
- `gh repo sync owner/your-fork -b main`
-----------


