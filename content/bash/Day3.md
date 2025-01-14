```bash
#! /usr/bin/bash

shopt -s extglob # enable linux shell to extended patterns matching in bash when we enable extglob you can use advenced pattern matching

# export LC_COLLATE=C

COMMENT
case $<variable> in

"case1")
	<Condition>
	;;
"case2")
	<Conditon>
	;;
"case3")
	<Condition>
	;;
esac

COMMENT:
read -p "Please Enter Your Name: " name

case $name in

"mahmoud")
	echo hello Manager
	;;
"ahmed")
	echo Hello Supervisor
	;;
"ismael")
	echo Hello Student
	;;
*)
	echo UNKNOWN USER
esac
*(pattern): match zero or more occurrence
?(pattern): match zero or one occurrence
+(pattern): match one or more occurrence
@(pattern): match exactly one occurrence
!(pattern): match anything except this pattern

read -p "Please Enter Your Name: " name

case $name in


+([a-z]|[[:space:]]))
	echo small letters
	;;
+([A-Z]))
	echo Capital letters
	;;
+([a-zA-Z0-9]))
	echo mix letters with numbers
	;;
+([0-9]))
	echo Numbers
	;;
*)
	echo UNKNOWN INPUT
esac



read -p "Please Enter Your Name: " name

case $name in


+([a-z])@([0-9]))
	echo small letters
	;;
+([A-Z]))
	echo Capital letters
	;;
+([a-zA-Z0-9]))
	echo mix letters with numbers
	;;
+([0-9]))
	echo Numbers
	;;
*)
	echo UNKNOWN INPUT
esac


while <condition>
do
	//logic
done

until <condition>
do
	//logic
done




declare -i num=0
while [ $num -lt 10 ]
do
echo $num
#num=$((num+1))
#((num++))
#num+=1

done

num=0
until [ $num -gt 10 ]
do
	echo $num
	((num++))
done

while true
do
read -p "Please Enter Your Name: " name

case $name in

[Ee][Xx][Ii][Tt])
read -p "Do you want to exit (y/n): " check
if [[ "yes" =~ $check ]]
then
	break
fi
	;;
+([a-z]|[[:space:]]))
	echo small letters
	;;
+([A-Z]))
	echo Capital letters
	;;
+([0-9]))
	echo Numbers
	;;
+([a-zA-Z]))
	echo mix letters
	;;
+([a-zA-Z0-9]))
	echo mix letters with numbers
	;;

*)
	echo UNKNOWN INPUT
esac
done



for <variable> in <list>
do

done



for name in ahmed mahmoud omar
do
	echo $name
done

for fileName in `ls $1`
do
	echo $fileName
done

for fileName in $(ls $1/*)
do
	#echo $fileName
chmod u-x $fileName
done

PS3="ENTER VALUE# "
select name in mahmoud ahmed ismael exit
do
case $REPLY in

"mahmoud")
	echo hello Manager
	;;
"ahmed")
	echo Hello Supervisor
	;;
"ismael")
	echo Hello Student
	;;
"exit")
	break
	;;
*)
	echo UNKNOWN USER
esac
done


# createDB selectDB renameDB DropDB
# createTB selectTB insertTB DropTB 

if [ -e ~/Courses/bash/Python-Nc/Database ]
then
	cd ~/Courses/bash/Python-Nc/Database
	echo "DBMS is ready"

else
	mkdir ~/Courses/bash/Python-Nc/Database
	cd ~/Courses/bash/Python-Nc/Database
	echo "DBMS is ready"
fi

 
select option in createDB SelectDB CreateTB exit
do
case $option in 
"createDB")
read -p "Please Enter Database name: " dbName
if [ -e $dbName ]
then
	echo "database is already exist"
else
	mkdir $dbName
	echo "Database is created successfully"
fi
;;
"SelectDB")
read -p "Please Enter Database name: " selectedDb
if [ -e $selectedDb ]
then
	cd $selectedDb
	echo "$selectedDb Database is selected"
else
	echo "Database is not exist"
fi
;;
"CreateTB")
read -p "Please enter table name: " tbName
if [ -e $tbName ]
then
	echo "table is already exist"
else
	read -p "please enter columns number to be created: " numCol
	pk=0
	for ((i=0;i<$numCol;i++))
	do
		line=""
		read -p "please enter column name: " colName
		line+=$colName
		read -p "please enter column Datatype (int/str): " colType
		line+=:$colType
		
		if [[ $pk -eq 0 ]]
		then
			read -p "Do you want to make this column pk (y/n): " checkPk
			if [[ "yes" =~ $checkPk ]]
			then
				line+=:PK
				pk=1
			fi	
		fi
		echo $line >> .$tbName"_metadata"
		
	done
	touch $tbName
	echo "table is created successfully"
fi
;;
esac
done


#declare -a arr=(1 9 99 8 55)

#echo ${arr[@]} # to print all array element
#echo ${arr[0]} # print first element
#echo ${arr[@]: 1} # skip first element in array

read -p "enter array size: " size

for ((i=0;i<$size;i++))
do
read -p "please enter element $i: " arr[$i]
done

declare -i sum=0
for num in ${arr[@]}
do
sum+=$num
done
echo "sum of the array is equal "$sum
((avg=$sum/$size))
echo "the averge is "$avg
echo ${arr[@]}


function hello(){
	echo "in hello fun"
}
hello

hello2(){
	echo "in hello2 fun"
}
hello2

hello(){
	echo "in hello2 fun"
	return 6
}
hello
returnVal=$?
echo the return is $returnVal

hello(){
	echo first arg: $1
	echo second arg: $2
	echo all arg: $@
	echo number of arg: $#
	((sum=$1+$2))
	return $sum
}
hello $1 $2
echo summtion is $?
```

























































































