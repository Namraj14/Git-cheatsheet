# 🧠 Git & GitHub Commands Cheat Sheet

-git init
-git add README.md
-git commit -m "first commit"
-git branch -M main
-git remote add origin https://github.com/Namraj14/Namraj14.git
-git push -u origin main


---
-git remote add origin https://github.com/Namraj14/Namraj14.git
-git branch -M main
-git push -u origin main

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

## ✅ Commands and Their Meanings

### 1. `git push --set-upstream origin master`

📌 **What it does:**

- Pushes your local `master` branch to the remote repository named `origin`.
- Sets the default tracking so future `git push` or `git pull` knows where to send or fetch from.

🗣️ **In simple terms:**  
“Hey Git, push my work from the `master` branch to GitHub, and remember this connection for the future.”

---

### 2. `git push -f origin main`

📌 **What it does:**

- **Force-pushes** your local `main` branch to the `origin/main` on GitHub.
- This overwrites the remote history with your local commits.

⚠️ **Use with caution!**

🗣️ **In simple terms:**  
“Hey GitHub, I know my work is different from yours, but replace your version with mine no matter what.”

---

### 3. `git branch -M main`

📌 **What it does:**

- Renames your current branch to `main`.
- `-M` means **force rename**, even if the `main` branch already exists.

🗣️ *“Change the name of my current branch to `main`, even if there was a branch called `main` already.”*

📘 This is useful if you started with `master` but want to switch to the modern default name `main`.

---

## 💡 What's the Difference?

| Command                            | Meaning                                                                 |
|-----------------------------------|-------------------------------------------------------------------------|
| `git push --set-upstream origin master` | Pushes and sets the default remote tracking for `master`               |
| `git push -f origin main`               | Forcefully overwrites the remote `main` branch with local changes     |

---

## ❓ FAQ – Git Rebase, Upstream & Push

### Q1: What is `--set-upstream`?
It links your local branch to a remote branch so you don’t have to type the full push command every time.

---

### Q2: What is `origin`?
`origin` is the default name Git gives to the remote repository (like GitHub).

---

### Q3: What is `rebase`?
Rebase moves your local changes on top of the latest remote changes — like reapplying your changes on a new base.

Example:
```bash
git pull --rebase origin main
