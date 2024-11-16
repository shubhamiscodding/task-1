git new task 1

# ts:1 install _and_ configure git
```
git config --global user.name "Your Name"
git config --global user.email "enter email"
```
### to Configure file to git we use this 

# ts:2 list git configuration
```
git config --list
```
### to view your configuration of your file

# ts:3 initialize a repo
```
mkdir MyProject<br>
cd MyProject
```
### to creat folder and to go into that folder
```
git init
```
### it intialize git in that folder 

# ts:4 creat new file do mutiple commits
1.
```
echo "text you eant to add in file" >> "file.ext"
```
### to creat a file add contant to it
2.
```
git add file.ext
```
### it add file to commit stage
3.
```
git commit -m "message"
```
### you can commit the file with this command
4.
```
echo "add a discription" >> file.ext
```
### to mamke changes to that file
5.
```
git add file.ext
git commit -m "undeted file"
```
### it stage the file and commit it again
# check status and log
1.
```
git status
```
### check the git repo's status wheather it is added for commit stage
2.
```
git log --oneline --graph --decorate
```
### it helps to show the history of git commit 
### oneline will show one line commit history
### graph will show branch strcute like line , branches ,mearged == |,/,*

# ts:5 creat and clone repo
1.creat a repo in github named exaple-repo
2.clone it locally
```
git clone http://codinggita.com/example-repo
```

# ts:6 understanding the git flow
## example Workflow
i.Make changes to a file in working directory:
```
echo "workflow example" >> workflow.md
```
ii.stage the file
```
git add workflow.md
```
iii.commit the file
```
git commit -m "add workflow example"
```

### PART:2

### ts:7  Branching and mearging
1.
```
git branch feature-login
git checkout feature-login
```
### creat new branch and goto that branch with the help of checkout or git switch
## or
```
git checkout -b feature-login
```
2.
```
echo "login page" >login.html
git add login.html
git commit -m "added login page"
```
### add new file and commit changes
3.
```
git checkout main
git merge feature-login
```
### checkout to go into main branch and now feature-login branch will be mearged with main branch.
### mearging feature branch into main branch

# ts:8 handling merge conflicts
1.
```
git branch example1
git branch example2
```
### Your working directory remains on the current branch. The new branches are created but not checked out.
### it will copy all the content of your working directory.
2.edit readme.md file's first line in both branches.
3.
```
git checkout main
git merge example1 
```
### merge example1 to  main branch
4.
```
git merge example2
```
### now if try to merge example2 to main it will creat conflict because both's first line is not empty.
### 5.first we have to solve inner conflict manually in readme.md ,then:
```
git add readme.md 
git commit -m "resolved merge conflict between example1 and example2"
```

# ts:9 renaming and deleting branch
1.Rename the branch
```
git branch -m old-branch-name new-branch-name
```
2.Delete a branch:
```
git branch -d feature-login
```
# part:3
# st:10 using git stash
1.Make changes to a file but don’t commit:
```
echo "Temporary work" >> temp.md
```
2.stash the changes
```
git stash
```
3.View stashed changes:
```
git stash list
```
4.Apply the stashed changes:
```
git stash apply
```
5.Drop the stash after applying:
```
git stash drop
```
