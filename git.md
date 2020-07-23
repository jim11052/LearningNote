### Sign last commit 
```sh
$ git commit --amend --signoff
```
```sh
git stash 
git checkout -b newbranchname
git stash 
git add .
git commit 
git push origin newbranchname:newbranchname

git checkout master
git branch -D removetokyo42ci
```
