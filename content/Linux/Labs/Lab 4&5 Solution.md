# Lab 4
### 6)Write two commands: first: to search for all files on the system that named .bash_profile. Second: sorts the output of ls command on / recursively, Saving their output and error in 2 different files and sending them to the background.
![[Pasted image 20241130003543.png]]
# Lab 5
### 1) Compress a file by compress, gzip, zip commands and decompress it again. State the differences between compress and gzip commands.

```bash
gzip lsfile -k
zip lsfile.zip lsfile
compress lsfile -k
```

![[Pasted image 20241130004607.png]]
![[Pasted image 20241130004908.png|500]]

| gzip                                        | compress                                              |
| ------------------------------------------- | ----------------------------------------------------- |
| gzip has faster and slower zipping commands | compress doesn't have quality of compression commands |
| gzip has testing the file after it's zipped | compress doesn't have it                              |
### 2) What is the command used to view the content of a compressed file.
```bash
zcat
```
### 3)Backup /etc directory using tar utility.

![[Pasted image 20241130005954.png|500]]
### 4)Starting from your home directory, find all files that were modified in the last two days.
![[Pasted image 20241130010150.png|500]]
### 5)Starting from /etc, find files owned by root user.
(from root directory)
```bash
:/$ sudo find -user root
```
### 6)Find all directories in your home directory.
![[Pasted image 20241130011522.png|500]]
### 7)Write a command to search for all files on the system that, its name is “.profile”.
![[Pasted image 20241130011626.png]]
### 8)Identify the file types of the following: /etc/passwd, /dev/pts/0, /etc, /dev/sda
- /etc/passwd : regular file
- /dev/pts/0 : character special file
- /etc : directory
- /dev/sda : no such file or directory 
### 9)List the inode numbers of /, /etc, /etc/hosts.
- / : 2
- /etc : 131073
- /etc/hosts : 131464
### 10)Copy /etc/passwd to your home directory, use the commands diff and cmp, and Edit in the file you copied, and then use these commands again, and check the output.
![[Pasted image 20241130012546.png|500]]
### 11)Create a symbolic link of /etc/passwd in /boot.

![[Pasted image 20241130012643.png|500]]

### 12)Create a hard link of /etc/passwd in /boot. Could you? Why?
![[Pasted image 20241130013239.png|500]]

Yes it was possible
Because the link was to the same partition. if it was to another partition it would fail
