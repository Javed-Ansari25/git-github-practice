# Git & GitHub Complete Notes (README)

## Introduction

Git is a version control system that helps track changes in code. GitHub is a cloud platform used to host Git repositories, collaborate with teams, review code, and manage projects.

---

## 1. Git & GitHub Basics Commands

### Check Git Version

```bash
git --version
```

Shows the installed Git version.

### Configure Git (First Time Setup)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Sets your identity for commits.

### Initialize Repository

```bash
git init
```

Creates a new Git repository in the current folder.

### Check Status

```bash
git status
```

Shows changed, staged, and untracked files.

### Add Files to Staging Area

```bash
git add .
git add filename.js
```

Stages all files or a specific file for commit.

### Commit Changes

```bash
git commit -m "Initial commit"
```

Saves a snapshot of staged changes.

### View Commit History

```bash
git log
git log --oneline
```

Displays commit history.

---

## 2. Git Terminologies

### Repository (Repo)

A project folder tracked by Git.

### Commit

A saved snapshot of changes.

### Branch

A separate line of development.

### Merge

Combines one branch into another.

### Clone

```bash
git clone repo-url
```

Downloads a remote repository to your system.

### Push

```bash
git push origin main
```

Uploads local commits to GitHub.

### Pull

```bash
git pull origin main
```

Downloads latest code and merges it.

### HEAD

Pointer to current branch or commit.

---

## 3. Git Branches and Conflicts

### Create Branch

```bash
git branch feature-login
```

Creates a new branch.

### Switch Branch

```bash
git checkout feature-login
```

Moves to another branch.

### Create + Switch Together

```bash
git checkout -b feature-login
```

Creates and switches in one command.

### Show All Branches

```bash
git branch
```

Lists local branches.

### Merge Branch

```bash
git checkout main
git merge feature-login
```

Merges feature-login into main.

### Merge Conflict

Occurs when two branches edit the same lines.

### Resolve Conflict

1. Open conflicted file.
2. Remove conflict markers.
3. Keep correct code.
4. Save file.
5. Run:

```bash
git add .
git commit -m "Resolved merge conflict"
```

---

## 4. Git Diff, Stash and Tag

### Git Diff

```bash
git diff
git diff filename.js
```

Shows code changes not committed yet.

### Git Stash

```bash
git stash
git stash list
git stash pop
git stash apply
```

Temporarily saves uncommitted work.

### Git Tag

```bash
git tag v1.0.0
git tag
git push origin v1.0.0
```

Used for versions/releases.

---

## 5. Git Rebase and Reflog

### Git Rebase

```bash
git checkout feature-login
git rebase main
```

Moves feature branch commits on top of updated main branch. Creates cleaner history.

### Git Reflog

```bash
git reflog
```

Shows all recent Git actions and HEAD movement.

### Recover Lost Commit

```bash
git reset --hard commitId
```

Restores repository to a previous commit.

---

## 6. Pushing Code to GitHub

### Add Remote Repository

```bash
git remote add origin repo-url
```

Connects local project with GitHub repo.

### Rename Default Branch

```bash
git branch -M main
```

Renames current branch to main.

### First Push

```bash
git push -u origin main
```

Pushes code and sets upstream.

### Next Pushes

```bash
git push
```

Pushes future commits quickly.

### Pull Latest Code

```bash
git pull
```

Gets latest changes from remote.

---

## 7. Open Source Contribution

### Step 1: Fork Repository

Create your own copy on GitHub.

### Step 2: Clone Fork

```bash
git clone your-fork-url
```

Downloads your fork.

### Step 3: Create Branch

```bash
git checkout -b fix-navbar
```

Use a separate branch for changes.

### Step 4: Make Changes + Commit

```bash
git add .
git commit -m "Fixed navbar issue"
```

### Step 5: Push Branch

```bash
git push origin fix-navbar
```

### Step 6: Create Pull Request

Submit your changes to the original repository.

---

## Important Interview Questions

### Difference Between Git and GitHub

* Git = Version control system.
* GitHub = Hosting and collaboration platform.

### What is Branching?

Used to develop features separately.

### What is Merge Conflict?

When same code area changed in two branches.

### What is Rebase?

Reapplies commits on updated base branch.

### What is Stash?

Temporary storage of unfinished work.

---

## Real Production Workflow

```bash
git checkout -b feature/payment
git add .
git commit -m "Added payment API"
git push origin feature/payment
```

Then create Pull Request, get code review, and merge.

---

## Quick Revision Commands

```bash
git init
git status
git add .
git commit -m "msg"
git branch
git checkout -b branch-name
git merge branch-name
git pull
git push
git stash
git tag v1.0
git rebase main
git reflog
```

---

## Final Tip

Practice these commands on one demo project. Real hands-on practice is the fastest way to become interview-ready.
