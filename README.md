# Github Playground
Testing Git
status
# Initialize repository
```
$ git init
```
# Check repository status
```
$ git status
```
# Add files/files
```
$ git add octocat.txt
---
$ git add .
---
$ git add '*.txt'
```
# Commit changes
```
$ git commit -m "Add cute octocat story"
```
# Check repository history
```
$ git log
```
# Associate local repository to remote repository
```
$ git remote add origin https://github.com/try-git/try_git.git
```
# Push changes to remote repository
```
$ git push -u origin master
```
# Pull down change from remote repository
```
$ git pull origin master
---
$ git pull
```
# Check changes from last commit
```
$ git diff HEAD
---
$ git diff
```
# Check staged changes
```
$ git diff --staged
```
# Staging a file
```
$ git add octofamily/octodog.txt
```
# Resetting the stage
```
$ git reset octofamily/octodog.txt
```
# Undo changes based from last commit
```
$ git checkout -- octocat.txt
```
# Create a branch
```
$ git branch clean_up
```
# Switch to brach
```
$ git checkout clean_up
```
# Remove files and stage the removal
```
$ git rm '*.txt'
```
# Merge brach to master
```
$ git checkout master
$ git merge clean_up
```
# Delete a branch
```
$ git branch -d clean_up
```