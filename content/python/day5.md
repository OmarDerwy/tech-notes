### 0.1.1	first class function?
![[Pasted image 20250303195435.png]]![[Pasted image 20250303195945.png]]
## 0.2	decorator

### 0.2.1	Revision on decorator
![[Pasted image 20250303200836.png]]

### 0.2.2	decorator chaining
![[Pasted image 20250303202811.png]]
### 0.2.3	common decorators ready to use
![[Pasted image 20250303204732.png]]
## 0.3	list comprehension
faster than for loop 
### 0.3.1	basic form
![[Pasted image 20250303203612.png]]
### 0.3.2	multiply numbers by 2
![[Pasted image 20250303203719.png]]
### 0.3.3	nested loop
![[Pasted image 20250303203841.png]]

### 0.3.4	create new list with special conditions
use ternary operator at the beginning
![[Pasted image 20250303204154.png]]
## 0.4	timer
![[Pasted image 20250303204431.png]]
### 0.4.1	testing the timer operator with list comprehension
![[Pasted image 20250303204543.png]]

## 0.5	dict comprehension
![[Pasted image 20250303204801.png]]
![[Pasted image 20250303204820.png]]
### 0.5.1	introducting zip()
![[Pasted image 20250303204858.png]]

### 0.5.2	aother example
![[Pasted image 20250303205032.png]]
answer
![[Pasted image 20250303205042.png]]

## 0.6	another reivision
![[Pasted image 20250303205544.png]]
## 0.7	high order functions
pure functions: dont change the original variable. and declare the changes thats made to it and don't procedure it
### 0.7.1	cases for high order functions
- data transformation which means apply a function on each element of the array and generate a new item
- data filtering which means select items in a list according to criteria
- data aggregation
![[Pasted image 20250303212842.png]]
![[Pasted image 20250303213039.png]]
All checks if all values in a list are true or not
![[Pasted image 20250303213114.png]]
any checks if any
![[Pasted image 20250303213149.png]]
checks if something is callable or not
### 0.7.2	map
![[Pasted image 20250303213340.png]]
### 0.7.3	anonymous function (lambda)
### 0.7.4	in a map
![[Pasted image 20250303213723.png]]
### 0.7.5	in a sorted
![[Pasted image 20250303214141.png]] 
![[Pasted image 20250303214200.png]]
### 0.7.6	in a filter
![[Pasted image 20250303214426.png]]
### 0.7.7	in a reduce
![[Pasted image 20250303214553.png]]
## 0.8	scopes
### 0.8.1	in an enclosed scope
If I do this
![[Pasted image 20250303222205.png]]
and I want to dictate that changes I do in the inner function affect the enclosing function but not the global.
then we use the nolocal thing
![[Pasted image 20250303222318.png]]![[Pasted image 20250303222532.png]]
LEGB heirarchy

## 0.9	generator
### 0.9.1	iterable vs iterator
![[Pasted image 20250304071407.png]]
### 0.9.2	convert str into an iterator
![[Pasted image 20250304072847.png]]

for loop essetially converts strings and other variables into an iterator for iterating through each loop of the for loop

if print iterator without next you get address

**closest use case for generator is the async aawait**

**the below example does not work**
![[Pasted image 20250304073611.png]]
do do this you need to
### 0.9.3	yield
generators dont use return but instead use yield keyword
yield returns an iterator istead of a normal value

but this below returns the same as return
![[Pasted image 20250304080232.png]]
we need store the iterator in a variable before we start using next on it
![[Pasted image 20250304080338.png]]
#### 0.9.3.1	using for loop with generator
![[Pasted image 20250304081118.png]]

### 0.9.4	building a range function yourself
![[Pasted image 20250304081406.png]]
### 0.9.5	use cases of generator
- async await
- coroutines
- iterate through a large list without reserving its entirely in memory
### 0.9.6	that's why map does this
![[Pasted image 20250304082128.png]]
map normally returns an iterator but when used with list() that it becomes a list
### 0.9.7	comparison between return and yield
![[Pasted image 20250304082359.png]]