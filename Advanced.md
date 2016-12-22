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
$ git rebase -i HEAD~3