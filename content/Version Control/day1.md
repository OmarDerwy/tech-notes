# 1	[[Version Control]] by [[Mahmoud Helmy]]
## 1.1	intro
application to track the source code of application from a to z
make collaboration easier between teams
### 1.1.1	why?
- help collaboriation
- accelerate prod delivery
- backup code
- keep track of modification
- work on branch without affecting main
### 1.1.2	terminology
- repository: database storing files
- server: project stored on it
- working copy: where you edit the code
- master/main: main branch
- commit: save changes  
## 1.2	centralized version control
every one can access the edit the resource at the same time in real time
major flaw is that if the centralized VCS goes down then nobody can access it.
## 1.3	Distributed version control
now code is split between local repo and remote repo. you commit changes into the local repo and push into remote

---

### 1.3.1	what happens if we edit a commit
it's id will change
### 1.3.2	if we edit a commit that exists in the remote, will it push?
no, you will have to force push.
## 1.4	git hands-on
### 1.4.1	initializtion
```
sudo apt install git
```
```
git init
```
all new files in a repo should be untracked
below gives you info
```
git status 
```
use
```
git add .
```
to add all the files to tracking
```
git config --global user.name
git config --global user.email
```
to get current branch
```
git branch
```
to rename branch
```
git branch -M <new name>
```
to commit
```
git commit -m "message of commit"
```
use to get a log of commits
```
git log
```
add and commit in the same step
```
git commit -am "message"
```
### 1.4.2	to add remote to local repo
```
git remote add origin <link ssh from repo>
```
to check if added remote
```
git remote -v
```
create ssh key once per machine for connection to github. to create it then
```
ssh-keygen -t ed25519 -C "preferable to put here email"
```
ED25519 is preferable for generating ssh key
go to

```mermaid
flowchart LR
profilepic --> sshskeyandgpg

```
when pushing
```
git push origin main
```