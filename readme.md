## Git Commands

### 1. Init
The git init command creates a new Git repository. 
```
git init
```

### 2. Add
The git add command adds a change in the working directory to the staging area.
```
git add .
```

### 3. Commit
Commit a snapshot of all changes in the working directory.
```
git commit -m "Commit message"
```
For editing last commit message.
```
git commit --amend
```

### 4. Status & log
The git status command displays the state of the working directory and the staging area.
```
git status
```
Git log is a utility tool to review and read a history of everything that happens to a repository. 
```
git log
git log --oneline
git log --oneline --graph --all
```

### 5. Push
The git push command is used to upload local repository content to a remote repository.
```
git push origin master
```

### 6. Pull
The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.
```
git pull origin master
```

### 7. Branch
A branch is a version of the repository that diverges from the main working project. It will create new branch.
```
git branch branch_name
```

### 8. Checkout
The git checkout command lets you navigate between the branches created by git branch.
```
git checkout branch_name
```
For creating new branch and HEAD pointer pointing to that new branch in one command.
```
git checkout -b branch_name
```

### 9. Merge
git merge is used to combine two branches. 
```
git merge branch_name
```
**Divergent Branch Error** :
Use merge no-ff stratergy to solve divergent branch conflict error. 
```
git pull origin main --no-ff
```

### 10. Rebase
Rebasing is the process of moving or combining a sequence of commits to a new base commit.
```
git rebase branch_name
```
**Interactive Rebase** :
Git interactive rebase allows you to change individual commits, squash commits together, drop commits or change the order of the commits.
```
git rebase -i HEAD~5
```
- pick (p for short), pick commit
- squash (s for short), which melds the commit into the - previous one (the one in the line before) 
- drop (d for short), remove commit
- reword(r for short) is used to edit commit messages.

### 11. Cherry-pick
Cherry-picking in Git stands for applying some commit from one branch into another branch. 
```
git cherry-pick commit_hash
```

### 12. Revert & Reset
The git revert command is a forward-moving undo operation that offers a safe method of undoing changes.
```
git revert
```
git reset is a powerful command that is used to undo local changes to the state of a Git repo.
```
git reset --hard
```

### 13. Stash
The git stash command takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy.
```
git stash
git stash save "message"
git stash list
git stash apply <stash id>
git stash pop
git stash clear
```

### 14. Tag
Tags are ref's that point to specific points in Git history.
```
git tag
git tag version1.0
```