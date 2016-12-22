# Github Playground
Testing Git
status
## Check help
```
$ git help
$ git help config
```
## Setting up git
```
$ git config --global user.name "Maurice Ilagan"
$ git config --global user.email "Maurice.Ilagan@email.com"
$ git config --global color.ui true
```
## Initialize local repository
```
$ git init
```
## Check local repository status
```
$ git status
```
## Add files/files
```
$ git add octocat.txt
$ git add .
$ git add --all
$ git add *.txt -- add all txt files in current directory
$ git add docs/
$ git add docs/*.txt
$ git add "*.txt" -- add all txt files in the whole project
```
## Commit changes
```
$ git commit -m "Add cute octocat story"
```
## Check repository history
```
$ git log
```
## Associate local repository to remote repository
```
$ git remote add origin https://github.com/try-git/try_git.git
```
## Push changes to remote repository
```
$ git push -u origin master
```
## Pull down change from remote repository
```
$ git pull origin master
---
$ git pull
```
## Check changes from last commit
```
$ git diff HEAD
---
$ git diff
```
## Check staged changes
```
$ git diff --staged
```
## Staging a file
```
$ git add octofamily/octodog.txt
```
## Resetting the stage
```
$ git reset octofamily/octodog.txt
```
## Undo changes based from last commit
```
$ git checkout -- octocat.txt
```
## Create a branch
```
$ git branch clean_up
```
## Switch to branch
```
$ git checkout clean_up
```
## Remove files and stage the removal
```
$ git rm *.txt
```
## Merge branch to master
```
$ git checkout master
$ git merge clean_up
```
## Delete a branch
```
$ git branch -d clean_up
```