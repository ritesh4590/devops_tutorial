# Git & GitHub Cheat Sheet

A quick reference guide for commonly used Git commands.

---

## Table of Contents

- [Configuration](#configuration)
- [Aliases](#aliases)
- [Cloning](#cloning)
- [Branching](#branching)
- [Committing](#committing)
- [Fetching & Pulling](#fetching--pulling)
- [Diffing](#diffing)
- [Logging](#logging)
- [Stashing](#stashing)

---

## Configuration

```bash
git config --list                              # List all configuration settings
git config --global user.name "user_name"      # Set global username
git config --global user.email "user_email"    # Set global email

git config --global --unset user.name          # Remove global username
git config --global --unset user.email         # Remove global email
```

---

## Check git remote

```bash
git remote -v
```

## Aliases

Create shortcuts for frequently used Git commands.

```bash
git config --global alias.<alias_name> <git-command>
```

> **Note:** Open Git Bash to create and use aliases.

**Example:**

```bash
git config --global alias.br branch   # Now "git br" runs "git branch"
```

---

## Cloning

```bash
git clone "<project-url>"                          # Clone a repository
git clone "<project-url>" .                        # Clone into the current folder
git clone --branch <branch_name> "<project-url>"   # Clone a specific branch
```

---

## Branching

```bash
git branch <branch_name>              # Create a new branch
git checkout <branch_name>            # Switch to a branch
git switch <branch_name>              # Switch to a branch (modern)

git checkout -b <branch_name>         # Create and switch to a new branch
git switch -c <branch_name>           # Create and switch to a new branch (modern)

git branch -D <branch_name>           # Force delete a branch
git branch -M <branch_name>           # Rename the current branch
```

---

## Committing

```bash
git commit -a -m "commit message"     # Stage all tracked changes and commit (skips git add)
git commit --amend                    # Modify the most recent commit (message or content)
```

---

## Fetching & Pulling

```bash
git fetch origin    # Download latest changes from remote (does NOT merge)
                    # After fetching, check status and merge manually

git pull            # Fetch + merge in one step (equivalent to git fetch + git merge)
```

---

## Diffing

```bash
git diff                              # Show changes in the working directory
git diff --staged                     # Show changes in the staging area
git diff origin/<branch_name>         # Compare local branch with remote branch
git diff <commitId_1> <commitId_2>    # Compare two specific commits
git diff --name-only                  # Show only the names of changed files
```

---

## Logging

```bash
git log --oneline    # Show a compact one-line-per-commit history
```

---

## Stashing

Stashing temporarily shelves changes so you can work on something else.

```bash
git stash              # Save current uncommitted changes to the stash
git stash list         # List all stashed entries

git stash apply        # Restore stashed changes (stash entry is kept — not recommended)
git stash pop          # Restore stashed changes and remove the entry (recommended)

git stash clear        # Delete all stash entries permanently
```

---

## SSH kay

How to genetare SSH key

```bash
ssh-keygen -t ed25519 -C <github account email>   # It will save the ssh key in local (Path will be diaplyed in terminal), yoy have to copy and paste the key in github setting SSH section

```

_Last updated: May 2026_
