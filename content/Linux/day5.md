# 1	[[Linux]] by [[Mahmoud Helmy]]
first file that runs when you log in `/etc/profile`
\# means root
$ means user 3ady
we also have `/etc/bash.bashrc` which is global config for bash
## 1.1	config files in home directory
- `.profile` or `.bash_profile`in redhat
- `.bashrc`
after the global files run the local ones do

so if you `su` to another user then .profile and then .bashrc runs

## 1.2	Processes
`top` view processes currently running on linux
`Q` to get out of the view
it is columned as follows:
- PID id for processor
- process owner
- priority | less is more priority
- `Nice` which affects the value of priority
	- done by `nice -n 10 top`
	- also done by`sudo renice <niceNo> -p PID`

`ps` processes running right now in the current running bash
	using `-e` brings the entire system processes
	using `-f` beings additional info
	using `aux` brings performance related info
	`PPID` is parent process ID

> [!NOTE]
> Parent process of the bash is the terminal

`pgrep` searchs through the processes
	exmaple: `pgrep bash`
	example answer: `8992`
- `-l` to include name in the output
- use `-x` to seach exactly the search parameter
`kill` ends processes using PID
- `-l` lists singals to send to the process
	- `SIGTERM` ask to end process and don't end if the process is relied upon by another(15)
	- `SIGKILL` force end the process (9)
`pkill` ends process by its name. It kills all processes that posses the same name
`Jobs` tells you what processes/applications running right now in the terminal

when you run a process that takes time. You could add `&` at the end of the command to send it to the background and `jobs` will display it

If you start a process that takes hold of your terminal and you want to send it to the background:
1. first `ctrl+z` to suspend the process
2. run `jobs` and find its number
3. `bg` which means background run it like this `bg %<number of the process>`
`fg` to get a process into the foreground

to `kill` a job you use `%` to denote the job like `kill %<number>`

## 1.3	piplining
pipeline takes the output of one command as input of another command

you have 3 types of redirection
- input
- output
- error
### 1.3.1	output
`cat /etc/passwd > passwd`
outputs the output of the `cat` into the new passwd
`echo hello > passwd` if passwd has content then this will overwrite
`echo hello >> passwd` if passwd has content this will append on it

### 1.3.2	error
errors are not an output and you can redirect it using
`2>`
like
`ls -R /etc passed 2>`


> [!NOTE]
> you have 2 files in /dev/ called `null` and `zero` and they are periodically emptied

### 1.3.3	input
`command < file`

## 1.4	misc
`wc /etc/passwd`
- line
- word
- character
`who` how is logged in now
`w` more info
`grep` search

`cut -d : -f1,3,5 /etc/passwd`
- `-d` specify the delimiter
- `-f1,3,5` get me the first, third, fifth columns
- file

`sort` sort the file (default: aphabetically line by line)
- `-t` delimiter
- `-k` field/column
- `-n` numeric
## 1.5	REGEX
`^h` starts with h
`.*` zero or more character
`h$` ends with bash