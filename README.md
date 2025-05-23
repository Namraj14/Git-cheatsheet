# Git-cheatsheet

📘 Git and GitHub Commands Cheat Sheet

🔧 Git Setup

git config --global user.name "Your Name"
git config --global user.email "you@example.com"

Set your global username and email address (used in commits).

📁 Starting a Git Repository

git init

Initialize a new Git repository in the current folder.

git clone https://github.com/username/repo-name.git

Clone a repository from GitHub to your local machine.

📄 Making Changes

git status

View the status of your working directory.

git add .

Add all changed files to staging.

git add filename

Add a specific file to staging.

git commit -m "Your commit message"

Commit the staged changes with a message.

🔁 Branching

git branch

List branches.

git branch branch-name

Create a new branch.

git checkout branch-name

Switch to a branch.

git checkout -b branch-name

Create and switch to a new branch.

git merge branch-name

Merge another branch into your current branch.

🌐 Working with Remote Repositories

git remote -v

List remote URLs.

git remote add origin https://github.com/username/repo-name.git

Link your local repo to a remote repo.

git push -u origin main

Push your local main branch to GitHub.

git push

Push your commits to the remote repository.

git pull

Fetch and merge changes from the remote repo.

🩽 Undoing Changes

git reset filename

Unstage a file.

git checkout -- filename

Discard changes in a file.

git revert commit-id

Revert a specific commit.

💃 Useful Logs

git log

View commit history.

git log --oneline

View commit history in one line per commit.

git diff

See changes not yet staged.

git diff --staged

See changes between staged and last commit.

🛠️ Stashing

git stash

Temporarily save all changes.

git stash pop

Reapply the last stash.

📌 Tags

git tag

List tags.

git tag v1.0

Create a tag named v1.0.

git push origin v1.0

Push a specific tag.

✅ Tip: Use git help <command> for any command to get detailed help.
