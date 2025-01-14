# 1	[[Linux]] by [[Mahmoud Helmy]]
## 1.1	user manipulation
* `userdel` deleted user from the config files but does not delete the home directory, use `-r` to delete everything related to this user

- `groupdel` deletes group from config files
## 1.2	file permissions
![[Drawing 2024-11-24 10.02.02.excalidraw]]
### 1.2.1	read permission
you can use cat, more, less, tail, head to read files but not alter or execute them
`r` in the permission view
### 1.2.2	write permissiions
you can use file editor to add lines and remove lines
`w in the permission view
### 1.2.3	execute permissions`
execute file
`x` in permission view
## 1.3	directory permissons
### 1.3.1	read
can view the directory with `ls` or otherwise
### 1.3.2	write
add or remove files and directories
### 1.3.3	execute
can `cd` on directory
## 1.4	permissions manipulation
### 1.4.1	chmod
- `chmod`
	- `u` users
	- `g` group
	- `o` others
	- `a` all
	- `-` removes permission
	- `=` overwrites permission
	- `+` adds permission
	- ',' do other permissions
**example**
`chmod u=r <file>`

> [!NOTE]
> if we use `sudo -s cd` to access a directlory that is read available to our current user. the root will get you inside the directory but once you switch back to the original user you will be kicked out of the directory

> [!NOTE]
> if we `touch` a file using `sudo` then the owner and group of the file are `root`

### 1.4.2	chmod alt
read = 4
write = 2
execute = 1
all = 7

**example**
`chmod 665 <file/dir>`

### 1.4.3	umask

4 digit number last 3 digits are mask for remove certain permissions from default

**example**
if we want to have 644 as default, then:
644
777
then
133
then do this:
`umask 0133`


> [!NOTE]
> maximum default permission for file is 666
### 1.4.4	chown
this command changes the ownership of files and directories
`sudo chown helmi file2`
to change group you need to do this
`sudo chown helmi:helmi file2`
to change only the group then
`sudo chown :helmi file2`

### 1.4.5	newgrp
new group switches your group from primary group to one of your supplementary groups to act on files 

`newgrp hamada`


> [!NOTE] Title
> you can access also other groups but you have to know their password
> to change password of group use `gpasswd` as `sudo`


## 1.5	manipulate process
ctrl c terminate
ctrl d close
ctrl z stop

## 1.6	man
manual for the entirely of linux
- section 1 is user commands
- section 5 is file formats and conversions
`man man` manual of man
- `-k` keyword
- `-a` all sections relation to search query

## 1.7	vi
is file editor in linux that works through the terminal
only available in emergency mode

vim is vi improved

you have to know about 3 mods of vi
- command mode
- insert mode
- last line mode
`i` for insert mode
`esc` to get back to command mode
`a` insert but with step forward
`A` insert but at the end of the line
`o`new line
`shift + I`  beginning of line
`shift + A` end of line
`u` undo
`ctrl+ r` redo
`0` beginning of line without insert mode
`home` `end` first and last of line without insert mode
`/` search for string `n` next search
`shift+n` previous search
`dd`delete line
`G` `L` last line
`H` first line
`ZZ` save and quit
`yy` copy line `yw` copy word
`p` paste after line `P`paste before line

`s` in command mode let's substitute a char and gets you in insert mode
`%s/word/another` search and replace substitutes once in a line use `/g` at the end to have it search in all the line 

`:1,2 co 3` copies line 1 and 2 and pastes them after 3
`:1,3 m 4` cuts line from 1 to 3 and pastes them after 4

## 1.8	environmental variables
`printenv` or `env
set by bash profile and bash rc`
without PATH you cannot run anything on linux

you can use `echo` to print the value of any variable
```bash
echo $USER
echo $SHELL
echo $PATH
```
once you close the terminal. some things reset like `umask` and `path`

so set an environmental variable

`car=basha` NO SPACES then `export car` to export it to environmental

use `$` to show, don't use it the `$`