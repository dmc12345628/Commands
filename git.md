Git
===

### Init 
git config --global user.email "your@email.com"
git config --global user.name "your name"

git init
git add <fileName>
git add .
git commit -m "comment of the modification"

git remote add origin <<URL.git>> 
git push -u origin master 
git push --set-upstream origin <<BRANCH NAME>>

git checkout -b <<BRANCH NAME>>
git checkout <<branch name>> (or <<commit name>>)
git chechkout .
git reset --hard 
git merge <<MASTER>> (or <<BRANCH>>)
git pull origin master 
	
git clone URL.git <<FolderName>>

COMMIT = Project version

// archive projet to zip
git archive HEAD --format=zip > /tmp/archive.zip
