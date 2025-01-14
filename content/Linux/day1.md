# [[Database]] by [[Amr ElHelw]]

steps to solve for database design may vary in detail from one person to another
## 0.1	Design
![[Pasted image 20241120090835.png]]
### 0.1.1	Requirement Gathering
What type of data are we dealing with?
- relational
- graph
- JSON
Do we need to aggregate and perform functions on the database frequenctly or is it OLTP (insert remove) type of need. Time series analysis?

Any speical requirements?


# 1	[[Linux]] Intro by [[Mahmoud Helmy]] 

We have a term called FOSS (Free/Open Source Software)
from the advantages:
- linux because open source bugs will be reported instantly
- you could monitize open source software by training, certificate, support, and many other meta aspects of the software itself.
- IBM bought RedHat for 34 Billion dollars. That means opensource is profitable.

examples of open source licenses:
- apache
- BSD
- MIT
- GPL

Several companies join forces to create one of the first OSs, Multex

companies pulled out and remained Bell Labs created the much improved Unix and they created it open-source.

Bell Labs changed the project source to closed source once.

Max was actually in the past build on Unix

Richard Stollman created the GNU project which were a multitude of open source libraries that were missing a kernel

Linus Trovalds was working on his graduation project which was the linux kernel

they both joined forces and created linux

slackware the first linux OS that came out

Distrowatch.com lists all the available distros

ISPs, eCommerce and numerous servers rely on Linux due to its unmatched security and performance

One of the most popular linux distrubutions is red hat

| Debian | Fedora |
| ------ | ------ |
| Ubuntu | RH     |
| Mint   | CentOS |
| PopOS  |        |
To install software we use package managers.

| Ubuntu | Fedora  |
| ------ | ------- |
| Apt    | Yum/dnf |
extensions in OS are different for executable

| Debuan | Fedora |
| ------ | ------ |
| .deb   | .rpm   |
Debian/Ubuntu is more userfriendly and Fedora is more server focused, more enterprise

Kernel

Core of OS
anything in the OS is the responsibility of the kernel
once linux is opened then kernel is stored on the RAM until the OS is closed

Shell
is the interface between you and the kernel
one of the most known shells is Bash

first we had sh, then ksh, then Bash

MacOS works with Zsh

Terminal is the GUI of shell

structure of commands

Command -> options -> argument

command: ls, ksh, useradd
option: -letter, --word
argument: more information that the command needs to continue execution

commands are seperated by a semicolon

for `ls` we can use `-a` to show hidden files and directories

in `ls -l`  blue listing is directory and has d in the beginning
anything white is file. green listing is file but executable
red is zipped or compressed

there are no extensions in linux 

everything is a file in linux

`uname` info about system `-a` all

`pwd` print working directory

directory tree of linux
`~` means the home directory of the current user
- /
	- /bin/ binary user commands
	- /opt/ third party tools
	- /boot/ responsible for booting the device and has the config files for booting the device
	- /root/ home directory of root superuser
	- /home/ home directory of users
	- /dev/ devices are all stored in this
	- /sbin/ super user commands
	- /etc/ config files of all linux
	- /srv/ services
	- /tmp/ temporary directory files and deleted automatically
	- /lib/ library that linux uses to help operate the system'
	- /usr/ use `which [path]` to know where the command will run from
		- /bin/
		- /include/
		- /lib/
		- /sbin/
	- /media/ external device 
	- /mnt/ external device mounting. when device is introduced it adds to /dev/ to determine a folder for which the device reads and writes into
	- /var/ constantly being updated and written on
		- /cache/
		- /log/
		- /spool/
		- /tmp/

