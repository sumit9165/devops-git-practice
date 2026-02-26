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
2. On-Local Command Line Interface .
To sync from your terminal, you must first configure a remote that points to the original repository.
- `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git`
- Fetch the latest changes: `git fetch upstream`
- Merge the changes into your local branch: `git merge upstream/main`
- Update your fork on GitHub: `git push origin main`

3. GitHub CLI
If you have the GitHub CLI installed, you can sync your fork with a single command:
- `gh repo sync owner/your-fork -b main`
-----
## What is the difference between git fetch and git pull?
-  Fetch Changes from Upstream: `git fetch upstream`
-  To keep your local repository up-to-date with the original repository, fetch the latest changes:
-  Push Changes to Origin: `git push origin main`
-  After merging the changes from the upstream repository, push your updated `main` branch to your forked repository on.

----
## `git merge <your branch>`
- It will merge branch into main

## `git stash`
- It will hide your changes from head and you can switch to another branch.

## `git stash pop`
- It will recover your changes.

## `git merge --squash <your branch>`
- It will merge all commits in one line with main branch

Below is a **structured reference table** covering:

* **What it is** (conceptually)
* **What it does** (technical effect)
* **Why we use it**
* **How to use it** (example)

---

# Branching

| Command                  | What It Is                     | What It Does                                             | Why We Use It                            | How To Use                  |
| ------------------------ | ------------------------------ | -------------------------------------------------------- | ---------------------------------------- | --------------------------- |
| `git branch`             | Branch listing tool            | Lists all local branches                                 | See current branches and active branch   | `git branch`                |
| `git branch <name>`      | Branch creation command        | Creates new branch pointer at current HEAD               | Start new feature without affecting main | `git branch feature-login`  |
| `git checkout <branch>`  | Branch switch command (legacy) | Moves HEAD to specified branch                           | Work on another branch                   | `git checkout develop`      |
| `git switch <branch>`    | Modern branch switch           | Changes current branch (cleaner alternative to checkout) | Clearer and safer branch switching       | `git switch main`           |
| `git switch -c <branch>` | Create + switch                | Creates branch and switches to it                        | Start new feature immediately            | `git switch -c feature-api` |
| `git merge <branch>`     | History integration command    | Combines specified branch into current branch            | Integrate completed feature              | `git merge feature-api`     |

---

# Remote

| Command                       | What It Is             | What It Does                               | Why We Use It                     | How To Use                                   |
| ----------------------------- | ---------------------- | ------------------------------------------ | --------------------------------- | -------------------------------------------- |
| `git clone <url>`             | Repository copy tool   | Downloads remote repo with full history    | Start working on existing project | `git clone https://github.com/user/repo.git` |
| `git remote -v`               | Remote inspection tool | Shows configured remote URLs               | Verify origin/upstream            | `git remote -v`                              |
| `git fetch`                   | Remote sync (no merge) | Downloads remote changes but doesn’t merge | Review remote updates safely      | `git fetch origin`                           |
| `git pull`                    | Fetch + merge          | Downloads and merges remote changes        | Update local branch quickly       | `git pull origin main`                       |
| `git push`                    | Upload command         | Sends local commits to remote              | Share work with team              | `git push`                                   |
| `git push -u origin <branch>` | Push + tracking setup  | Pushes branch and sets upstream            | Simplify future pushes            | `git push -u origin feature-login`           |

---

# Merging & Rebasing

| Command                | What It Is                 | What It Does                             | Why We Use It                          | How To Use             |
| ---------------------- | -------------------------- | ---------------------------------------- | -------------------------------------- | ---------------------- |
| `git merge <branch>`   | History combining method   | Creates merge commit combining histories | Preserve branch history                | `git merge feature-ui` |
| `git rebase <branch>`  | History rewriting method   | Moves commits to new base                | Cleaner, linear history                | `git rebase main`      |
| `git rebase -i HEAD~3` | Interactive history editor | Lets you squash, edit, reorder commits   | Clean up commit history before pushing | `git rebase -i HEAD~3` |

---

# Stash & Cherry-pick

| Command                    | What It Is        | What It Does                                | Why We Use It                             | How To Use                |
| -------------------------- | ----------------- | ------------------------------------------- | ----------------------------------------- | ------------------------- |
| `git stash`                | Temporary storage | Saves uncommitted changes                   | Switch branches without committing        | `git stash`               |
| `git stash pop`            | Restore stash     | Reapplies stashed changes and removes stash | Resume paused work                        | `git stash pop`           |
| `git cherry-pick <commit>` | Commit copy tool  | Applies specific commit onto current branch | Reuse specific fix without merging branch | `git cherry-pick a1b2c3d` |

---

# Reset & Revert

| Command                    | What It Is                       | What It Does                                  | Why We Use It                    | How To Use                |
| -------------------------- | -------------------------------- | --------------------------------------------- | -------------------------------- | ------------------------- |
| `git reset --soft HEAD~1`  | History rewind (non-destructive) | Moves HEAD back, keeps changes staged         | Rewrite last commit              | `git reset --soft HEAD~1` |
| `git reset --mixed HEAD~1` | Default reset                    | Moves HEAD back, unstages changes             | Redo commit cleanly              | `git reset HEAD~1`        |
| `git reset --hard HEAD~1`  | Full reset                       | Moves HEAD back, deletes changes              | Discard local commits completely | `git reset --hard HEAD~1` |
| `git revert <commit>`      | Safe undo                        | Creates new commit reversing specified commit | Undo pushed commits safely       | `git revert a1b2c3d`      |

---

# Recovery & Safety

| Command      | What It Is    | What It Does             | Why We Use It                           | How To Use                                  |
| ------------ | ------------- | ------------------------ | --------------------------------------- | ------------------------------------------- |
| `git reflog` | Reference log | Shows all HEAD movements | Recover lost commits after reset/rebase | `git reflog` then `git reset --hard <hash>` |

---

# Summary

* **Branching** = parallel development.
* **Remote commands** = collaboration.
* **Merge** = combine histories.
* **Rebase** = rewrite history.
* **Stash** = temporary save.
* **Cherry-pick** = copy specific commit.
* **Reset** = move branch pointer.
* **Revert** = undo safely.
* **Reflog** = emergency recovery tool.

---
