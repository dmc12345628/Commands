Git Tutorial
============

## User access
Set user access from local repository to remote repository
```git
git config --global user.email "your@email.com"
git config --global user.name "your name"
```

## Prepare local repository
* Init local repository
```git
git init
```

* Connect to remote repository
```
git remote add origin <<URL.git>>
```

* Add local files to local repository 
```git
git add [fileName] // Add a specific file
git add .
```

* Commit changes
```git
git commit -m "comment of the modification"
```

* Add local changes to remote repository
``` 
git push -u origin master
```

* Add local changes in new local branch. It adds the local branch to remote repository.
```
git push --set-upstream origin [Branche name] 
```

## Working with branches
* Create a branch
```
git checkout -b [Branch name]
```

* Change to another branche or commit
```
git checkout [branch name/commit name]
```

* Discard all not committed changes
```
git checkout .
```

```
// archive projet to zip
git archive HEAD --format=zip > /tmp/archive.zip
git reset --hard

git merge [master/branch name]
git pull origin master 
git clone URL.git [FolderName]
```