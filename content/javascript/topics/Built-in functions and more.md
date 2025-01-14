```
instructor:: [[Mennatullah Hamdy]]
date:: 2024-12-24
```

regex101 essential site for learning and testing regex

after some time of not typing anything
# 1	date
date functions support adding days, hours or minutes to the one we have by get
```javascript
var date = new Date('August 19, 1975 23:15:00')

var day = getDay()

date.setDay(day+40)
```
# 2	errors
> [!NOTE]
> Take note that when comparing reference with reference you will always get a false
> `[] == []` will always be false

## 2.1	reference error
usually appears when calling a variable that is not declared
## 2.2	syntax error
mistyping the basic suntax of javascript will net that error
## 2.3	type error
type error is when the same happens with a method

using `throw` the command will throw an error
```js
var error= ErrorMessage("This is an error")
throw error
```
you can use methods `.name` and `.message`
### 2.3.1	try catch finally
you can use this is to catch errors and resolve them without becoming incaught errors

if there is more than one error you can use an object to catch them
```js
try{
x = 1
console.logc(x)
} catch (error) {
console.log(error)
} finally {
console.log("anyways")
}
```
## 2.4	objects
if we create an object with properties. adding a value into a property that wasn't defined in the object throws an error

when creating a function inside an object that has properties.
you access these properties inside the function using the `this.`

if you return an object from a function and then create an instance of that function then you can add properties to the function by will.


### 2.4.1	keys
```js
console.log(Object.keys(obj))
```

### 2.4.2	delete
```js
delete obj.name
```
if the key doesn't exist then it doesn't throw an error (note: typescript does)

### 2.4.3	entries
returns multiple arrays each have an index for key and index for value
```js
console.log(Object.entries(obj))
```
# 3	functions
## 3.1	immediately invoked function expression
wrap around your function round braces and add an invoke at the end
```js
(function (){
	console.log('one time function');
})()
```
object of the function has a length property. It's useless

## 3.2	argument defaults
you can set an argument = number to set it as default without sending argument in call

## 3.3	length in function
there is an `arguments.length` in function that gives you the number of passed arguments in a function. Since functions don't throw an error if you pass arguments more than the function allows.
