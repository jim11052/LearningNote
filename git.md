### Sign last commit 
```sh
$ git commit --amend --signoff
```
### Merge request to origin/master
```sh
git stash 
git checkout -b `new-branch-name`
git stash list 
git stash pop
git add .
git commit ...
git pull --rebase
git push origin `new-branch-name`:`new-branch-name`

git checkout master
git branch -D `new-branch-name`
```

### Submodule
```sh
git submodule update --init --recursive
```

### Modify commit if alerady pushed 
```sh
git rebase -i HEAD~5    # then modify pick to edit
git add . 
git status              # then follow the instructions 
```
