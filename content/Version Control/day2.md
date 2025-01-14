# 1	[[Version Control]] by [[Mahmoud Helmy]]
## 1.1	cont.
to restore file to beginnin of vommit
```
git restore <file>
```
to return from staged
```
git restore --staged <file>
```
to view changes of each commit use
```
git show
```
to get back to a previous commit use two ^^ to get back two commits #iti/inquire/vc
```
git reset --soft HEAD^^
```
to delete commit with its changes ]
```
git reset --hard HEAD^
```
to get log of all things you did
```
git reflog
```
to revert undo changes you did in a certain commit
```
git revert <commit id>
```
to get diff between staged and original
```
git diff
```
to add changes to your last commit
```
git commit --amend -m "message here"
```
to create new branch
```
git branch dev
```
to work on new branch
```
git checkout dev
```
if you create a branch and add commits to it then merge to main without having any commit be made to made then merge type is fast-forward

to solve conflicts. Open the offending file and choose the correct change.

to resolve conflicts in in rebase fix them and then
```
git rebase --continue
```
git pull is a mix between git fetch and git merge

if you want to fetch and rebase instead of merge then
```
git pull -r
```
if we want to delete branch, it refuses if it finds it was not fully merged
```
git branch -d dev
```
for force delete
```
git branch -D dev
```
to create and checkout to a branch
```
git checkout -b newbranch
```
create tag
```
git tag "name"
```
delete tag with `-d`
use `-m` to add description to your tags
use `:branch` to specify which branch to add the tag to.
## 1.2	.gitignore
files that should not be uploaded to github and should be added here
- node_modules
- .env