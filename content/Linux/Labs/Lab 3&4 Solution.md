# Lab 3
## 8)

| shell | initialization file                    | System wide init file |
| ----- | -------------------------------------- | --------------------- |
| sh    | it can use  `~/.profile`               | `/etc/profile`        |
| ksh   | `~/.kshrc` and before it `~/.profile`  | `/etc/profile`        |
| bash  | `~/.bashrc` and before it `~/.profile` | `/etc/profile`        |
## 9)
in the file `/.profile`
![[Pasted image 20241126194545.png]]
![[Pasted image 20241126202956.png]]

# 10)
the `\` allows the next character to escape the interpreter of the shell. If for example we press enter after the `\` then we create a newline that we can write on without executing the command

We can change the `>` by changing the PS2 value![[Pasted image 20241126210010.png]]

## 11)
by adding 
```bash
alias ls='ls -l'
```
at the end of the `/.bashrc` file
![[Pasted image 20241126210331.png]]
# Lab 4
## 1)
![[Pasted image 20241126211907.png]]
## 2)
![[Pasted image 20241126212002.png]]
## 3)
![[Pasted image 20241126212734.png]]
## 4)
![[Pasted image 20241126212859.png]]
## 5)
![[Pasted image 20241126213146.png]]
## 7)
![[Pasted image 20241126213243.png]]
## 8)
![[Pasted image 20241126213919.png]]
## 9)
- Nothing happens
- ![[Pasted image 20241126214339.png]]
- It outputs one line because ls 1 file outputs one file ![[Pasted image 20241126214446.png]]
## 10)
![[Pasted image 20241126214514.png]]
## 11)
![[Pasted image 20241126214821.png]]
## 12&13)

![[Pasted image 20241126214917.png]]
## 14)
![[Pasted image 20241126215052.png]]
## 15)
![[Pasted image 20241126215126.png]]
## 16)
![[Pasted image 20241126215726.png]]
## 17)
![[Pasted image 20241126215902.png]]
## 18)
![[Pasted image 20241126215958.png]]
## 19)
```bash
pkill -u derwy
```