## git reset

**undo add command** and keep changes in working directory

`git reset` 

**undo commit and redo** when you realize the commit is not complete 

`git reset --soft HEAD^`

`//edit + add`

`git commit -a -c ORIG_HEAD` -- keep the message unchange

`git commit -a ORIG_HEAD` -- want to edit the message

**undo a commit, make it a topic branch**

`git branch topic/wip`

`git reset --hard HEAD~3`

`git checkout topic/wip`

**undo a commit, make it a topic branch**

`git branch topic/wip`

`git reset --hard HEAD~3`

`git checkout topic/wip`

**undo commit permanently**

`git reset --hard HEAD~3`

**undo a merge** and delete all changes in working directory

`git reset --hard`

**undo a merge** and keep changes in working directory

`git reset --merge ORIG_HEAD`

**hotfix** in the middle of coding features

`//doing codeing in feature1 branch with half cooked code`

`git commit -a -m "snapshot WIP"`

`git checkout master`

`git checkout -b hotfix1`

`//fix bug here`

`git commit -a -m "fix the bug"`

`git checkout feature1`

`git reset --soft HEAD^`

`git reset`

**reset a single file**

`git reset -- file1.txt`

**keep change in working tree while discarding some previous commits**

`git tag start`

`git checkout branch1'

`//edit + commit to branch 1`

`// continue to edit for branch 2, then you realize that branch2 should not depend on branch1`

`git checkout -b branch2`

`git reset --keep start`

**Create new commit that undoes all of the changes** made in , then apply it to the current branch.

`git revert <commit>`

## git log

**View history of one file**

`git log -- file1.txt`

**View log with filename status**

`git log --name-status`

**Show log** of change in local directory

`git reflog`

**Show full log**

`git log -p <commit>`



## git diff

**Compare working directory and index**

`git diff`

Show difference between working directory and last commit.

`git diff HEAD`

Show difference between staged changes and last commit

`git diff --cached`

## branch

**Create new branch**

`git branch <branch-name>`

**Create new branch and switch to it**

`git checkout -b [branch name]`

**Delete local branch**

`git branch -d <branch-name>`

**Delete remote branch**

`git push origin --delete <branch-name>`

**Rename a branch**

`git branch -m [old branch name] [new branch name]`

**Merge a branch into target branch**

`git merge [source branch] [target branch]`





