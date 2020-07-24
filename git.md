### Sign last commit 
```sh
$ git commit --amend --signoff
```
### Merge request to origin/master
```sh
git stash 
git checkout -b "new-branch-name"
git stash 
git add .
git commit 
git push origin "new-branch-name":"new-branch-name"

git checkout master
git branch -D "new-branch-name"
```
### Submodule
```sh
git submodule —init —recursive
```
