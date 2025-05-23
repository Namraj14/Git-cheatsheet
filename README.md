# 🧠 Git & GitHub Commands Cheat Sheet

A simple and structured guide to essential Git and GitHub commands.

---

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

