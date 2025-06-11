# 🧠 Git & GitHub Commands Cheat Sheet

### How to Create a New Git Repository and Push to GitHub

```bash
# Initialize a new Git repository
git init

# Add the README.md file to staging
git add README.md

# Commit the changes with a message
git commit -m "first commit"

# Rename the default branch to 'main'
git branch -M main or git branch -m master main (renaming from master to main)

# Add the remote GitHub repository URL
git remote add origin https://github.com/Namraj14/Namraj14.git

# Push the local 'main' branch to the remote repository and set upstream
git push -u origin main


# Add the remote repository (if not already added)
git remote add origin https://github.com/Namraj14/Namraj14.git

# Push the 'main' branch to GitHub and track it
git push -u origin main

or

# Your local branch is master and u want to push in the main in remote branch
git pull --rebase origin main and  
git push -u origin master:main
---
A simple and structured guide to essential Git and GitHub commands.

## 🔧 Git Setup

- Set your username:
  - `git config --global user.name "Your Name"`

- Set your email:
  - `git config --global user.email "you@example.com"`

---

## 📁 Create and Clone Repositories

- Initialize a new local Git repository:
  - `git init`

- Clone an existing repository:
  - `git clone <repository-url>`

---

## 📌 Stage and Commit Changes

- Check the status of your working directory:
  - `git status`

- Add a file to staging area:
  - `git add <file-name>`

- Add all files:
  - `git add .`

- Commit the staged changes:
  - `git commit -m "Your commit message"`

---

## 🔀 Branching

- List all branches:
  - `git branch`

- Create a new branch:
  - `git branch <branch-name>`

- Switch to a branch:
  - `git checkout <branch-name>`

- Create and switch to a branch:
  - `git checkout -b <branch-name>`

- Merge another branch into the current one:
  - `git merge <branch-name>`

- Delete a branch:
  - `git branch -d <branch-name>`

---

## 📤 Push and Pull

- Pull the latest changes from remote:
  - `git pull origin <branch-name>`

- Push local changes to remote:
  - `git push origin <branch-name>`

- First time push (sets upstream):
  - `git push -u origin <branch-name>`

---

## 📦 Stashing

- Save changes without committing:
  - `git stash`

- Apply the last stashed changes:
  - `git stash pop`

---

## 🧽 Reset and Revert

- Discard all changes in the working directory:
  - `git reset --hard`

- Revert a specific commit:
  - `git revert <commit-hash>`

---

## 🔍 Logs and History

- Show commit history:
  - `git log`

- Show a compact history with graph:
  - `git log --oneline --graph`

- Show the content of a specific commit:
  - `git show <commit-hash>`

---

## 🌐 Remote Repositories

- View current remotes:
  - `git remote -v`

- Add a new remote:
  - `git remote add origin <url>`

---

## 🛠️ Common Issues

- **Detached HEAD**:
  - Solution: `git checkout <branch-name>`

- **Merge Conflicts**:
  - Solution: Manually resolve conflicts → `git add .` → `git commit`

---

## ✅ Best Practices

- Always pull before you push to avoid conflicts.
- Write clear and meaningful commit messages.
- Keep your branches organized and delete unused ones.
- Use feature branches for new features and bug fixes.


# 🚀 Git Push Command Cheat Sheet with Explanation

This markdown explains the use of common `git push` commands like `--set-upstream` and `-f` with examples and a simple FAQ section for quick revision.

---
