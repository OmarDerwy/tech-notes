# Lab 2

## 13)
![[Pasted image 20241124142053.png|400]]

## 14)
![[Pasted image 20241124142330.png|400]]
## 15)
![[Pasted image 20241124144617.png|400]]
## 16)
### 16.1)
![[Pasted image 20241124145008.png|400]]
### 16.2)
![[Pasted image 20241124145141.png|400]]
### 16.3)
the maximum permission a file can have is everything except execute which is 666
when it comes to directory, the maximum permissions for it is 777
### 16.4)
![[Pasted image 20241124145532.png|400]]
## 17)
### 17.1)
for file: you need read permission to be able to copy it
for directory: you need to execute to able to access it and write to write to it

### 17.2)
to copy a file you need to have read permissions on the file

### 17.3)
you don't anything but the parent directory's write permissions to delete a file
### 17.4)
to list directory you need read permissions of the directory
### 17.5)
to view file content you need file read permission
### 17.6)
to modify a file's content you need write permission

## 18)
**Read only**
![[Pasted image 20241124155513.png|400]]
![[Pasted image 20241124155601.png|400]]
## 19)
the x permission for the file gives permission to execute that file to that it can run if it's a program or a script
the x permission for a directory gives permission to `cd` to that directory

# Lab 3

## 1)
![[Pasted image 20241124160725.png|400]]
## 2)
- in the vi command mode
	- move the cursor up using the `k`button
	- move the cursor down using the `j` button
	- search for the word age using `/age` in the command mode
	- step to line 5 using `:5`
	- delete the line you are on using `dd` and since I was on line 1 and deleted the line then line 5 became line 4 so to delete line 4 `:4d`
	- using the key `A`
## 3)
using this `cat /etc/shells`
## 4)
`printenv`
## 5)
`bash -c 'printenv'`
## 6)
`echo $<variable>`
## 7)
`echo $0`
 

