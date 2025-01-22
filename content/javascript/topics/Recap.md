# 1	variable declaration
- var: ECMA5
	- you can redeclare it multiple times no problem
- let: ECMA6
	- throws error when redeclaration #iti/interview-question/javascript

language is actually interperted but more accurately it is JIT compiled #iti/interview-question/javascript first thing it checks
	cannot redeclare block scoped

- const block scoped also. it also made it possible to declare variables that cant be changed or reassigned
# 2	hoisting
the compiler takes all function and cariable declarations and puts them up at the top of the scope.
but the value doesn't get hoisted with the declaration #iti/interview-question/javascript 

var variables get hoisted and if used before they're defined then they output undefined

let also gets hoisted but it doesn't output undefined if accessed before it's declared. instead it outputs an error

not defined if variable wasn't declared anywhere at all

null: you made it null
undefined: wasn't initially set
NaN: not a number


anything added to string is converted to string #iti/interview-question/javascript 
NaN is not equal anything even itself
```js
1+1 = 2
"1"+1 = "11"
1+false=1 // all booleans turn into numbers
1+"false" // 1false
1+true //2
1+null //1 because null acts like zero
1+undefined // NaN
"1" + undefined //1undefined
undefined + undefined //NaN
1/0 // infinity
1-"1" //0 <-- number
1-false // 1
1-"hamada" // NaN
null==undefined // true
null===undefined // false
typeod(NaN) // number
```

lexical scope is the normal scope in JS

means that if the value isn't found inside the scope then it searches outside the scope for the variable #iti/interview-question/javascript 

if you call a variable at the begginning of a function and it initialized with var later on and is initialized outside the scope then it will not see the outside variable and **undefined** #iti/interview-question/javascript 

every function has a return and if not then its return is undefined.

if you declare a variable without either var or let or const then it is defined as global. but it **doesn't get hoisted** 

functions are essentially objects. so if you defined properties onto functions and call them then you can retrieve those properties no problem. #iti/interview-question/javascript 

# 3	functions
## 3.1	anonymous functions

anonymous functions don't get hoisted]

typeof(null) // object

all arguments are stored in `arguments`

### 3.1.1	arrow functions
shorthand of regular anonymous functions 

variable `arguments` not in arrow function #iti/interview-question/javascript 

# 4	this
this always references the parent object of the current scope.


> [!NOTE]
> > in an arrow function it almost always returns the window.
> > unless it is enclosed with a normal function

```js
```
```js
```
```js
```
```js
```
