# Github Playground
Testing Git

# Try Git
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
## Add file/files/directory
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
## Remove remotes
```
$ git remote rm origin
```
## Push changes to remote repository
```
$ git push -u origin master
```
## Pull down change from remote repository
```
$ git pull origin master
$ git pull
```
## Check changes from last commit
```
$ git diff HEAD
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
## Remove files and stage the removal
```
$ git rm *.txt
```

# Staging & Remote
## Skip staging and commit
```
$ git commit -a -m "Modify readme"
```
## Undo the last commit, put changes into staging
```
$ git reset --soft HEAD^
```
## Undo the last commit and all changes
```
$ git reset --hard HEAD^
$ git reset --hard HEAD^^ -- undo the last 2 commits and all changes
```
## Amend the last commit
```
$ git commit --amend -m "Modify readme & add todo.txt"
```
## Show remote repositories
```
$ git remote -v
```
## Password caching
```
http://help.github.com/articles/set-up-git
```
# Cloning and Branching
## Clone a repository
```
$ git clone https://github.com/codeschool/git-real.git
$ git clone https://github.com/codeschool/git-real.git git-demo -- different folder name
```
## Create a branch
```
$ git branch clean_up
```
## Switch to branch
```
$ git checkout clean_up
```
## Create and move to branch
```
$ git checkout -b admin
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
# Collaboration Basics
## Conflict between remote and local
```
$ git pull
$ git push
```
# Branching
## Create a remote branch then push to remote
```
$ git checkout -b shopping_cart
$ git push origin shopping_care
```
## Get all branches
```
$ git pull
```
## List all remote branch
```
$ git branch -r
```
## Remote show (status of all branches)
```
$ git remote show origin
```
## Removing a remote branch
```
$ git push origin :shopping_cart
```
## Deleting a branch
``` 
$ git branch -d shopping_cart
$ git branch -D shopping_cart -- delete branch event with uncommited changes
```
## Clean up stale branches
```
$ git remote prune origin
```
## Link up a local branch (staging) to remote branch (master)
```
$ git push origin staging:master
```
## List all tags
```
$ git tag
```
## Checkout code at commit (tag)
```
$ git checkout v0.0.1
```
## Add a new tag
```
$ git tag -a v0.0.3 -m "version 0.0.3"
```
## Push new tags
```
$ git push --tags
```
## Update local branch/tag info
```
$ git fetch
```
