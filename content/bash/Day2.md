```bash

#! /usr/bin/bash

# file that take execute permission 

#ps
#echo $$ # current process


# Sourcing put . before script or source

#cd ~
#pwd

# two methods to print variable
#name=mahmoud
#echo $name
#echo ${name: 1} #skip to the first letter
#echo ${name: -2} # will get last two character

# shell doesn't know number only strings

#x=10+10
# casting 
#((x=10+10))
#y=$((10*10))
#let z=2*2
# to declare variable as int
#declare -i q=8*8
#echo $x
#echo $y
#echo $z
#echo $q

#echo "current process: " $$
#echo "name of file: " $0
#echo "number of args: " $#
#echo "print all args: " $*
#echo "print all args: " $@
#echo "first args: " $1
#echo "second args: " $2

#test "ali" = "alii" && echo True || echo False

#[ "ali" = "ali" -a "b" = "b" ] && echo True || echo False

#[ "ali" = "alii" -o "b" = "ba" ] && echo True || echo False


#[[ "ali" = a* && "b" = "ba" ]] && echo True || echo False

#[[ "ali" = a* || "b" = "ba" ]] && echo True || echo False

#[[ "yes" =~ "se" ]] && echo True || echo False

# -gt greater than
# -ge greater than or equal
# -le less than or equal
# -lt less than
# -eq equal
# -ne not equal


#[[ 10 -ge 11 ]] && echo True || echo False

#((10==9)) && echo True || echo False

#export 
# '' ""
#echo 'the value is: \$g'
# read
#echo "Please Enter Your Name"
#read -p "Please Enter Your Name: " name
#echo $REPLY
#echo "Hello $name"
#if
<<COMMENT
if <Condition>
then
	// logic if true
	
elif <Conditon>
then
	logic of second true condtion 
else
	//logic if false
fi

read -p "Please Enter Your Name: " name

if [[ $name = "mahmoud" ]]
then
	echo Hello Manger
elif [[ $name = "ahmed" ]]
then
	echo Hello Supervisor
else 
	echo UNKNOWN USER
	
fi


# Need to make script to know if argument is file or dir

if [[ $# -gt 0 ]]
then
	if [[ -f $1 ]]
	then
		echo File
	elif [[ -d $1 ]]
	then
		echo dir 
	else
		echo missing file or dir
	fi
	

else
	echo invalid Args
fi
COMMENT
#echo $g
if [[ $# -gt 0 ]]
then
	if [[ -f $1 ]]
	then
		echo File
		if [[ -r $1 ]]
		then
			echo Readable
		fi
		if [[ -w $1 ]]
		then
			echo writable
		fi
		if [[ -x $1 ]]
		then
			echo excutable
		fi
	elif [[ -d $1 ]]
	then
		echo dir 
		if [[ -r $1 ]]
		then
			echo Readable
		fi
		if [[ -w $1 ]]
		then
			echo writable
		fi
		if [[ -x $1 ]]
		then
			echo excutable
		fi
	else
		echo missing file or dir
	fi
	

else
	echo invalid Args
fi

```









