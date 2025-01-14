# 1	[[Linux]] by [[Mahmoud Helmy]]
## 1.1	Alias
change a command's syntax to something else
**example:**
```bash
alias rm="rm -i"
```
we already have aliases like
```bash
ll
# which is present in /.bashrc like
alias ll='ls -AlF'
```
use `unalias` to remove a command from alias
## 1.2	inode
inode is a data structure that is not available for the end user.

every file has a number that can be called 'primary key'
#iti/inquire/linux 
this PK is in a table that has all the files in it. the columns after the PK contain:
- type of file
- the file's permissions
- number of links

You cannot put a file from a partition to another partition with the same inode
view inode number by using `ls -i`
view the entire data of the file using `stat <file>`

`df` shows partitions of the device use `-i`

if a large file occupies that partition. It still has one inode to access it but the next file will be assigned an inode that is no incremental to the last one
**example**:
if a BIG file has inode 666000
next file will NOT have inode 666001
## 1.3	links
### 1.3.1	soft link
symbolic link is a simple shortcut similar to .lnk files in windows
creats a new inode with a new file type and everything
how to do it
`ln -s <path of file> <path to create link in>` for soft link or symblolic link both paths have to be absolute paths, not relative
if we `ls -l` the link we will find `l` at the beginning of the permissions

symbolic links don't have permissions, they only link you to the original file and its original permissions

links in `ls` are colored blue

if you delete the source file then the file is gone
## 1.4	hard link
hards links create another pointer to the same file in the partition.
Both files are pointers to the file if you delete either of them. It will only delete the link and the other file is available
```bash
ln <file> <path>
```
absolute file path is not necessary for this one

you can only create hard links to file and not directory

## 1.5	searching
## 1.6	locate
search in its database and look for the file there
```bash
sudo updatedb
```
```bash
locate <file>
```
supports regex
## 1.7	find
searches in the actual directories and files themselves
```bash
find ~/ -perm 664
```
```bash
find ~/ -perm 777 -type d
```
```bash
find ~/ -maxdepth 1
```
```bash
find ~/ -mindepth 2
```
```bash
find ~/ -mtime +2
```
use the previous to search for mod more than 2 days ago
or use `-2` to search for files 2 days ago or less
if exactly `2` then exactly 2 days ago

## 1.8	archiving and compressing
### 1.8.1	archiving
```bash
tar -cf data.tar <path to archive
```
`-c` create
`-f` specify file name
`-t` to view files in tar file
`-x` extract files out of the archive
### 1.8.2	compress
there is 
`compress`
`uncompress`

`gzip`
`gunzip`

use `zcat` to read files

`bzip2`
`bunzip2`
use  `bzcat` to read files compressed by bzip2

use `zip` to use zip you can archive and compress the file
use `unzip -l <file>` to list the files inside
`unzip <file>` to unzip files

## 1.9	packages
```bash
# use this to search
apt search <package to search>
# use this to update repos
apt update
# use this to upgrade all your packages
apt upgrade
```
