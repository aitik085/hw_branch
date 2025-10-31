```
mkdir hw_branch
touch merge.sh
touch rebase.sh
touch README.md
cd hw_branch
git init
git remote add origin https://github.com/aitik085/hw_branch.git
git status
git remote -v
git add .
git commit -a -m "Prepare for merge and rebase"
git branch -M main
git push -u origin main
git commit -a -m "add code to README"
git push -u origin main
git checkout -b git-merge
git commit -a -m "merge: @ instead * [git-merge]"
git commit -a -m "merge: use shift [git-merge]"
git push -u origin git-merge
git checkout main
git merge git-merge
git push -u origin main
git checkout aab195db79c9b9ca79d030e33d7837a671137bdd
git checkout -b git-rebase
git commit -a -m "git-rebase 1 [git-rebase]"
git commit -a -m "git-rebase 2 [git-rebase]"
git push -u origin git-rebase
git checkout main
git checkout git-rebase
git rebase -i main
git add rebase.sh
git rebase --continue
git add rebase.sh
git rebase --continue
git push -u origin git-rebase -f
git checkout main
git merge git-rebase
git commit -a -m "add All commands to README"
```