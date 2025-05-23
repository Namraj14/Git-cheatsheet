# Git & GitHub Commands Cheat Sheet

A handy reference for essential Git and GitHub commands used in daily development workflows.

---

## 🔧 Git Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
Set your identity for all repositories on your machine.

🆕 Create or Clone a Repository
Create New Repository
bash
Copy
Edit
git init
Initialize a new local Git repository.

Clone Existing Repository
bash
Copy
Edit
git clone https://github.com/username/repo.git
Clone a remote GitHub repository to your local machine.

📂 Basic File Operations
bash
Copy
Edit
git status
Check the status of your working directory.

bash
Copy
Edit
git add <filename>
git add .
Stage file(s) for commit.

bash
Copy
Edit
git commit -m "Your commit message"
Commit staged changes.

bash
Copy
Edit
git rm <filename>
Remove file from Git and working directory.

🔄 Branching
bash
Copy
Edit
git branch
List all branches.

bash
Copy
Edit
git branch <branch-name>
Create a new branch.

bash
Copy
Edit
git checkout <branch-name>
Switch to a branch.

bash
Copy
Edit
git checkout -b <branch-name>
Create and switch to a new branch.

bash
Copy
Edit
git merge <branch-name>
Merge a branch into your current branch.

bash
Copy
Edit
git branch -d <branch-name>
Delete a branch.

🔁 Pull & Push
bash
Copy
Edit
git pull origin <branch-name>
Fetch and merge changes from the remote repository.

bash
Copy
Edit
git push origin <branch-name>
Push local commits to the remote repository.

📥 Stash Changes
bash
Copy
Edit
git stash
Temporarily save changes.

bash
Copy
Edit
git stash pop
Apply the latest stashed changes.

🧼 Reset & Revert
bash
Copy
Edit
git reset --hard
Reset your local working directory to the last commit.

bash
Copy
Edit
git revert <commit-id>
Revert a specific commit (creates a new commit).

🕵️ History
bash
Copy
Edit
git log
View commit history.

bash
Copy
Edit
git log --oneline --graph --all
Pretty log view with graph.

bash
Copy
Edit
git show <commit-id>
See details of a specific commit.

🌐 GitHub Specific
bash
Copy
Edit
git remote -v
View remote connections.

bash
Copy
Edit
git remote add origin https://github.com/username/repo.git
Link your local repo to a remote GitHub repo.

bash
Copy
Edit
git push -u origin main
Push your first commit and set upstream.

🚨 Troubleshooting
Detached HEAD:
Run git checkout <branch-name> to return to a branch.

Merge conflicts:
Open conflicting files, resolve conflicts, then git add . and git commit.

