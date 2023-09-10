# git-lesson


# Global config 
- git config --global user.name "Gleb Mojeico" 
- git config --global user.email "g.mojeico@gmail.com"

- git config --list --global




# Git add and commit 

- git add first_file
- git commit -m "add first file



# Git add + commit all files (without untracked files )

- git commit -am "git add + git commit without untracked files "


# Git add + commit for one file (not for untrack)

- git commit -m "add + commit for one file " my_file_name



# Git show last commit or commit with hash 

- git show
- git show 4faa7df241ef2f8353c8ad61d86a565256b1234b


# Delete file + add deleted file  -> rm file + git add file  

- git rm index.html






# Git show all branches + last commit 

- git branch -v 



# Git create new branch 

-  git branch feature

# Git switch to branch 

- git checkout feature
- git checkout -b feature                    -> create branch + checkout 
- git checkout -f branch_name                -> delete uncommit files and changes 
- git checkout -B branch_name 3j34r91fe      -> checkout to branch with commit hash (return old version of branch) 
- git checkout 438j83gjf3 file_name_and_path -> checkout file from commit (return file to "old"" version )




# Git save uncommited files before checkout to another branch 

- git stash - save your uncommited files without commit
- git stash pop - return uncommited files 


# Git merge 

- git merge branch_name          -> merge branch_name to current branch

- fit merge --squash branch_name -> merge branch_name to current branch 


# Git reflog - track branches


- git reflog  

33225e1 (HEAD -> main, origin/main, origin/HEAD) HEAD@{0}: commit: reafactoring main
fbf0325 (origin/feature) HEAD@{1}: merge feature: Fast-forward
b2d07d5 HEAD@{2}: checkout: moving from feature to main
fbf0325 (origin/feature) HEAD@{3}: commit: udpate README.md
3cd0dc3 HEAD@{4}: commit: udpate README.md
5b63175 HEAD@{5}: commit: update README file
c740932 HEAD@{6}: reset: moving to HEAD
c740932 HEAD@{7}: checkout: moving from main to feature




# Git restore branch from reflog

- git branch feature HEAD@{2}


# Git remove untracked files 

- git clean -dxf  ->   d folers | x file from .gitignore | f files 

# Git reset (doesn't work with untracked files)

- git reset --hard commit_hash  -> reset to commit_hash
- git reset --hard HEAD         -> reset to last commit


# Git diff 

- git diff master feature  -> compare master with feature 

- git diff       -> compare index with working directory 
- git diff HEAD  -> compare HEAD (last commit ) with working directory


# Git cherry-pick

- git cherry-pick hash_commit  -> copy commit to current branch


# Git rebase 


- git rebase master   - rebase master to current branch (move all commits from master to current branch, but compress all commits from master to one commit  )
- git rebase --abort  - return to version before rebase if we have problems

- git rebase 


git merge  - create new commit in your branch 
git rebase - attach your BRANCH to last commit of master # https://mcs.mail.ru/blog/rukovodstvo-po-git-zolotoe-pravilo-i-drugie-osnovy-rebase 

