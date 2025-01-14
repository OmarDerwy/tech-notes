---
date: 2024-12-28T00:00:00.000+02:00
instructor: "[[Mennatullah Hamdy]]"
---
ES6 was the biggest update that happened to JS
ES5 was the second biggest revision
# 1	variable declaration (let/const)
- the biggest misconception is that let doesn't get hoisted. That's wrong
- let and const hoist the value normally but they don't put the value with 'undefined'
- we cannot redelcare a variable in the same scope.
- block scoped not function scoped (any braces means that variable in a new scope)
- const doesn't allow reassignment of its value

> [!NOTE]
> use const constantly until you find that you need to reassign it

# 2	Arrow functions
- arrow functions are not hoisted much like anonymous functions
- it's a short syntax for anonymous functions
- if you have 1 input variable then no () necessary
- if function is one line then no {} necessary
- return is implicit in one line
- we use arrow functions everywhere except inside objects.
- This in arrow function brings back global object and not the function itself. thats why we don't use them in objects or in non-method functions
# 3	Spread operator
![[Pasted image 20241228094933.png]]
```js
//in console the result is
arr = [1,2,4,3,5,6]
```
- one of the uses of spread operators is specifying that we need a copy of an array not a reference.
**they are also used in objects**

![[Pasted image 20241228095539.png]]
one of the uses also is sending argments to a function that are in an arrray without the hassle of converting to arguments
# 4	For/of
like for in but doesn't need object.
It loops through values of an iterable instead of keys
# 5	Map
![[Pasted image 20241228102913.png]]
like objects but preserve the order of entrants
## 5.1	clear, delete and has
clear removes all elements from the map but preserves the map
delete removes a certain key/value
has returns if a certain key exsists
# 6	Set - like Map but for arrays not objects
unique values
![[Pasted image 20241228103610.png]]
removes duplicates
![[Pasted image 20241228104221.png]]
# 7	Classes - OOP is not as good as other langs
# 8	a bunch of concepts
# 9	reduce
![[Pasted image 20241228115939.png]]
# 10	array and object destructor
## 10.1	array destructor
![[Pasted image 20241228123950.png]]
## 10.2	object destructor
![[Pasted image 20241228124032.png]]
You can also rename variable after extracting it from the object
## 10.3	examples
![[Pasted image 20241228124629.png]]
![[Pasted image 20241228124823.png]]
# 11	modules
#iti/inquire/js commonjs vs esmjs
![[Pasted image 20241228130546.png]]
# 12	promise
![[Pasted image 20241228132018.png]]
![[Pasted image 20241228132048.png]]
![[Pasted image 20241228132604.png]]
## 12.1	chained promise
![[Pasted image 20241228133826.png]]
#iti/inquire/js how to manipualte then and catch better
## 12.2	promise methods
all, race, allSettled, resolved, reject
# 13	async and await
![[Pasted image 20241228135904.png]]
use it to have functions wait for other functions to finish before starting execution
![[Pasted image 20241228140212.png]]
example from MDN