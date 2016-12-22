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
# Purging History
## Create a backup of the repository
```
$ git clone petshop petshop-filter
```
## Tree filter
```
$ git filter-branch --tree-filter 'git rm -f password.txt' -- --all
```
## Index filter
```
$ git filter-branch --index-filter 'git rm --cached --ignore-unmatch password.txt'
```
## Delete commits that are empty
```
$ git filter-branch -f --prune-empty -- --all
```
# Working Together & Cherry-Pick
## Line Endings
```
$ git config --global core.autocrlf input -- Linux
$ git config --global core.autocrlf true -- Windows
```
## .gitattributes
```
text=auto
*.html text
*.png binary
*.sh text eol=lf
*.bat text elo=crlf
```
## Cherry-Pick
```
$ git checkout master
$ git cherry-pick 53212e2
$ git cherry-pick --edit 53212e2 -- edit commit message
$ git cherry-pick -x 5321 -- add source SHA to commit message
$ git cherry-pick --signoff 5321 -- adds current user's name to commit message
```
## Cherry pick multiple commits
```
$ git cherry-pick --no-commit 53212e5 55ae374
$ git commit -m "Updates"
```
# Submodules
## Add a Submodule
```
$ git submodule add https://github.com/milagan/test.git
$ git commit -m "Add Test submodule."
```
## Update a Submodule
```
$ cd test
$ git checkout master
$ git commit -am "Testing submodule"
$ git push

-- parent directory
$ git add Test
$ git commit -m "Update submodule"
$ git push
```
## Initialize submodule after clone
```
$ git submodule init
```
## Pull down submodule
```
$ git submodule update
```