### 1. What is Git and why is it used?  
**Answer:** Git is a version control system that tracks changes in files and helps multiple developers collaborate.  
**Example:** Like saving multiple drafts of your essay to keep history.

---

### 2. What is the difference between Git and GitHub?  
**Answer:** Git is software to track changes locally; GitHub is a cloud platform to store and share Git repos online.  

---

### 3. Explain the Git workflow.  
**Answer:** You modify files → stage changes (`git add`) → commit changes (`git commit`) → push to remote (`git push`).  

---

### 4. What is a commit?  
**Answer:** A commit is a snapshot of your project at a point in time with a message explaining the changes.  

---

### 5. What is branching in Git?  
**Answer:** Creating a separate line of development to work on new features or fixes without affecting the main code.  

---

### 6. How do you create and switch to a new branch?  
**Answer:**  
git checkout -b new-branch

### 7. What is the difference between `git merge` and `git rebase`?

- **git merge**  
  - Combines the changes from one branch into another.  
  - Preserves the full history of both branches, creating a *merge commit*.  
  - History shows the true branching structure with all commits intact.  
  - Example:  
    ```
    git checkout main
    git merge feature-branch
    ```
  - Useful when you want to keep a record of the feature branch’s separate history.

- **git rebase**  
  - Moves or reapplies your commits on top of another base commit (usually main branch).  
  - Rewrites history to create a linear, cleaner sequence of commits.  
  - Avoids merge commits, making history look like a straight line.  
  - Example:  
    ```
    git checkout feature-branch
    git rebase main
    ```
  - Useful for a clean, linear project history but **do not rebase shared branches** as it rewrites history.

---
### Difference Between git merge and git rebase

- **git merge**  
  Combines two branches by creating a new "merge commit."  
  Keeps all history and shows that branches happened.  
  Safe to use when working with others.

- **git rebase**  
  Moves your branch's commits on top of another branch.  
  Makes history look like one straight line (no merge commits).  
  Good for cleaning up your work before sharing, but don't rebase shared branches.

---

**Example:**  
```bash
# Merge example
git checkout main
git merge feature-branch

# Rebase example
git checkout feature-branch
git rebase main

### What does "keeps history" and "makes history" mean in Git?

- **Keeps history**  
  This means Git saves all the past changes and shows exactly when and how branches split and came back together.  
  You can see the full timeline of what happened in your project.  
  Example: When you use **git merge**, Git adds a special “merge commit” that connects the histories, so nothing is lost.

- **Makes history** (or rewrites history)  
  This means Git changes the recorded order of commits to make it look like changes happened in a straight line, without branches.  
  It can make the history easier to read but changes the commit record.  
  Example: When you use **git rebase**, Git takes your commits and re-applies them on top of another branch, creating new commit records with new IDs.

---

### Simple analogy:

- **Keeps history** is like saving every step you took on a map, showing every turn and detour.  
- **Makes history** is like drawing a straight line from start to finish, ignoring the detours to make it look simple.



**Summary:**  
- Merge **preserves** history with merge commits; rebase **rewrites** history for a linear flow.  
- Merge is safer for shared branches; rebase is good for cleaning up your local commits before merging.


8. When would you use git stash?
Answer: To temporarily save unfinished changes without committing them.
Example: You are working on a feature but need to switch branches quickly.

9. How do you undo a commit that hasn’t been pushed?
Answer: Use git reset --soft HEAD~1 to undo last commit but keep changes staged.

10. What is the purpose of .gitignore?
Answer: It tells Git which files or folders to ignore (not track).

11. How do you resolve merge conflicts?
Answer: Manually edit conflicting files, then stage and commit them.

12. What does git pull do?
Answer: Fetches changes from remote and merges them into the current branch.

13. How is git fetch different from git pull?
Answer: Fetch only downloads changes; pull fetches and merges automatically.

14. What is a remote repository?
Answer: A repository hosted on a server or cloud (like GitHub) to share code.

15. How do you link a local repo to a remote repo?
Answer:
git remote add origin <repo-url>

16. What does git clone do?
Answer: Copies a remote repository to your local machine.

17. What is a detached HEAD state?
Answer: When HEAD points to a specific commit, not a branch, so commits aren’t saved to a branch.

18. How do you check the status of files?
Answer:
git status

20. How do you view the commit history?
Answer:
git log

21. What is the difference between git reset and git revert?
Answer: Reset moves HEAD backward (rewriting history); revert creates a new commit that undoes changes.

22. How do you delete a remote branch?
Answer:
git push origin --delete branch-name

23. How do you delete a local branch?
Answer:
git branch -d branch-name

23. What is a pull request (PR)?
Answer: A request to merge code changes from one branch to another, often reviewed before merging.

24. How can you check the difference between commits?
Answer:
git diff commit1 commit2

26. What is the purpose of the staging area?
Answer: It holds changes before you commit them.

27. What command stages all changes?
Answer:
git add .

27. How do you rename a branch?
Answer:
git branch -m old-name new-name

28. What is a fast-forward merge?
Answer: A simple update when the branch can be moved forward without creating a new commit.

29. What is the use of git tag?
Answer: To mark specific commits as important, often for release versions.

30. How do you revert a file to its last committed state?
Answer:

git checkout -- filename
31. How do you set up tracking for a remote branch?
Answer:

git push --set-upstream origin branch-name
32. What is the difference between origin and upstream remotes?
Answer: origin is your forked repo; upstream is the original repo you forked from.

33. How do you fetch changes from upstream?
Answer:
git fetch upstream

35. What is the HEAD in Git?
Answer: The pointer to the current commit or branch you’re working on.

36. What are submodules in Git?
Answer: Repositories inside repositories, used to include external projects.

37. How can you squash commits?
Answer: During rebase, use git rebase -i to combine commits into one.

38. What happens if you force push (git push -f)?
Answer: Overwrites remote history; can cause problems if others rely on it. Use carefully!

39. What does git cherry-pick do?
Answer: Applies a single commit from one branch into your current branch.

40. How do you ignore file mode changes in Git?
Answer:
git config core.fileMode false

40. How do you list all branches?
Answer:
git branch

42. How do you view remote URLs?
Answer:
git remote -v

42. What is GitHub Actions?
Answer: GitHub’s automation for running workflows like tests and builds on push or PR.

43. What is a .gitkeep file?
Answer: An empty file used to keep empty folders tracked in Git (which ignores empty folders).

44. How do you undo changes in the staging area?
Answer:
git reset HEAD filename

46. What is git blame used for?
Answer: To see who last changed each line in a file.

47. What is the default branch name in new Git repos?
Answer: main (older repos used master).

48. How do you stash and apply changes?
Answer:
git stash
git stash apply

48. What is Git LFS?
Answer: Large File Storage to manage big files (like videos) with Git.

49. How do you create a new empty branch without history?
Answer:
git checkout --orphan new-branch

51. How do you fix “detached HEAD” state?
Answer: Checkout a branch:
git checkout branch-name
