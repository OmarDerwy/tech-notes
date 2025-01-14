# 1	[[bash|Bash]] by [[Mahmoud Helmy]]
## 1.1	intro
we can use shebang to specify which shell to use in executing the following script
```bash
#! /usr/bin/bash
```
when we run a new script the OS starts a new shell to execute it. to tell it to execute in the current process or the current shell, we use this
```bash
$ . <path of script>
# or
$ source <path of script>
```

of course once we run source run bash script while we change the shebang `bash` to `ksh` for example. it will ignore the shebang and instead execute int he currently running shell.

## 1.2	echo
of course we know how echo works from [[2024-11-24#1.8 environmental variables]]
we can use curly braces to manipulate which parts of a string to print:
```
echo ${name: 1} # skip to first letter
echo ${name: -2} # get last 2 char
```
## 1.3	number variable
use this casting:
```
((x=10+10))
```
or this:
```
let z=2*2
```
to declare static datatype:
```
declare -i q=8*8
```


> [!NOTE]
> There is no float in bash
> to display decimal numbers we use pipelining into bc like this
> `echo 5/2 | bc -l`

```bash
echo	"current process: " $$
echo	"name of file: " $0 
echo	"number of args: " $#
echo	"print all args: " $*
echo	"print all args: " $@
echo	"first args: " $1
echo	"second args: " $2
```
## 1.4	test
this tests a condition and outputs something:
```bash
test "ali" = "alii' && echo True || echo False
```
we can use instead []
```bash
[ "ali" = "alii' ] && echo True || echo False

```
we can use `-a` for AND and `-o` for OR
![[Pasted image 20241211100447.png]]

to use [[meta characters]] you need to use double brackets `[[]]`
and to additionally use [[regex]] use `~` after the equal sign


> [!NOTE] 
>
>  Upon using `[[]]` then we use `$$` and `||` instead of -o and -a

![[Pasted image 20241211101425.png]]

# 1	[[bash]] by [[Mahmoud Helmy]]

## 1.1	switch case in bash
![[Pasted image 20241212095451.png]] ![[Pasted image 20241212100618.png]]
```bash
shopt -s extglob # to enable the above
```
## 1.2	case
## 1.3	while
## 1.4	until
## 1.5	for
## 1.6	select
![[Pasted image 20241212113549.png]]![[Pasted image 20241212113752.png]]