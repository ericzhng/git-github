
# Instructions to use for git repo

## if you have a project directory, but want to crates a bare repo to host this locally
git clone --bare project project.git

## show all branches both locally and remotely
git branch -a

## you can use following to view the repo
git remote -v

## you can also remove origin from the bare repo
git remote remove origin

## you can now add remote in your project repo

git remote add origin E:\2_WorkDir\work-Git\git_tut.git
git remote add origin https://github.com/ericzhng/git2.git

## create github repo (needs to install github cli tool)
gh repo create ericzhng/git2 --public
git push -u origin main

## push a new branch "feature" to github
git push -u origin feature
git push origin my-feature:feature	## local branch/remote branch

## to push changes
git pull origin main
git push origin main

## associate remote branch with local branch
git push -u origin calc-divide

## to merge
git checkout main
git merge calc-divide
git branch --merged

git push origin main

## delete merged branch
git branch -d calc-divide
git push origin --delete calc-divide

## to stage
git add -A
git add .

## only do this when you are only developer, will change git history
git commit --amend -m "complted substract"

## commit to wrong branch
git branch subtract-feature
git checkout subtract-feature
git log
git cherry-pick [a hash]
git reset --soft / --hard / --mixed 

## get rid of untracked files, after hard reset
git clean -df

## print command history
git reflog

## keep untracked changes while switch to new branch
git switch -c feature

## stash
git add -A
git stash save "message"
git stash list

## set remote 
git remote set-head origin -d
git push –set-upstream origin new-branch
git push --all origin
git push --all --set-upstream origin

## setup a repo locally
git init

## rename local branch
git branch -m master main

## relink remote repo
git remote set-url origin git@github.com:User/project-new.git
