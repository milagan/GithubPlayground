# Github Playground
Advanced Git

# Interactive Rebase
## Alter commits in the same branch
```
$ git rebase -i HEAD~3
-- reword - rewording the commit
-- edit - split the commit
```
## Splitting the commit
```
$ git rebase -i HEAD~3
$ git reset HEAD^ -- after changing to edit
$ git add file1.html
$ git commit -m "Add file1.html"
$ git add file2.html
$ git commit -m "Add file2.html"
$ git rebase --continue
```
## Squashing/merging the commits
```
$ git rebase -i HEAD~3 -- squash
```
# Stashing
# Save files to stash
```
$ git stash save
$ git stash save "Test Message"
```
# Apply changes from stash
```
$ git stash apply
```
# Show list of stashes
```
$ git stash list
```
# Apply a specific stash
```
$ git stash apply stash@{1}
```
# Drop stash
```
$ git stash drop
```
# Apply and drop
```
$ git stash pop
```
# Staging area not to be stashed
```
$ git stash save --keep-index
```
# Stash untracked files
```
$ git stash save --include-untracked
```
# More details on stash (can use log params)
```
$ git stash list --stat
$ git stash show
```
# Create a new branch from stash
```
$ git stash branch admin stash@{0}
```
# Blow away all stashed
```
$ git stash clear
```