# 1	[[Linux]] by [[Mahmoud Helmy]]
I am very sick today so maybe not much note taking.

- are we going to get redhat certification?
- tips and tricks for linux or ubuntu in general.
## 1.1	display files in linux
- cat
- less
- more
- head
	- -#
- tail
	- +#
- ls list files in directory
	- -a list hidden
	- -d directory
	- -l permissions
- cd move through directories
## 1.2	wildcards
- *
- ?
- \[range]
- {incrementfrom...to...by}
## 1.3	manipulate files and directory
- touch create file
- mkdir create dir
- `cp` copy file
	- `cp file newdir/` copy to new location
	- `cp file file2 file3 newdir/`
	- `cp file{1..9} newdir/` 
	- `cp dir newdir/` you need to add `-r` to copy directories
- `mv` 
	- `mv file1 file2` using it as rename no problem
	- `mv file1 dir/file2` move and rename
- in `cp` and `mv`
	- `-i` to confirm if there is overwrite or not
- `rm file removes file immediately and permenantly
	- use `i` to ask for confirmation
	- use `-r` for recursive
- `rmdir` removes empty directiry
## 1.4	user config files
- /etc/passwd
- /etc/shadow/
- `ls -a /etc/skel` these are skeleton files that build a new user home directory

## 1.5	user manipulation commands
- `useradd`
- `su - hamada` switch user
- `whoami` who is the current user
- `usermod` modify user
	- `-g` modify primary group
	- `-G` modify secondary group
	- `-a` append user with group without removing user from other groups. Example: `usermod -aG group user`
- `groupadd` add new group
- `chage` changes password expiration for users