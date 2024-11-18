# **Git Task List 02 - Notes**

## **Git Commands**


git branch <branch-name> ->create branch and if you are in any branch it will be copied

git checkout <branch-name> ->to switch the branch

git branch -m <old-name> <new-name> -> rename the branch

git branch -d <branch-name> -> to delete the branch

git branch -D <branch-name> -> to force delete

git push origin --delete <branch-name> -> to delete branch remote

git stash ->  to temporarily save your uncommitted changes (both staged and unstaged) and clean your working directory without committing the changes.

git stash apply -> Restores the changes without removing the stash.

git stash drop ->  Deletes a specific stash.

git rebase -i HEAD~3 ->

git cherry-pick <commit-hash> ->  to apply a specific commit from one branch into another branch without merging the entire branch

git reset --soft HEAD~1

git reset --hard HEAD~1

git diff -> shows the differences between files in your working directory and the index (staging area), between the index and the last commit, or between two commits.

# Example .gitignore file

node_modules/

*.log

### git config --global alias.st status

-=>allow you to create shorthand commands for frequently used Git commands or combinations of commands
### git config --global alias.cm commit

git config --global --get-regexp alias

git tag -a v1.0 -m "Version 1.0 release"

git push origin v1.0
