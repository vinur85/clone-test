# Purge past commits and remove big files


## get past 3 commits for all branches

```
git clone --depth 3 git@github.com:ijin/clone-test.git 
cd clone-test
git remote set-branches origin '*'
git fetch --depth 3 -vvv
git branch -a
du -sh .
```

`1.7M .`

## remove big files and checkout relevant brnaches

```
git filter-branch --index-filter 'git rm -rf --cached -r --ignore-unmatch photo.JPG' HEAD --all
git checkout 1
git checkout 2
git checkout 3
du -sh .
```

`1.1M .`

## change 'origin' to new repo and push

```
git remote set-url origin git@github.com:ijin/clone-test-lite.git
git push --all
```

## clone from new repo

```
git clone git@github.com:ijin/clone-test-lite.git
cd clone-test-lite
du -sh .
```

`100K .`



a
b
c
d
e
f
g
