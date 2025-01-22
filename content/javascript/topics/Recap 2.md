# 1	Promise
Promise is a solution to the problem of call back hell.

for further explanation of the callback hell problem, refer to the nasr video explaining the topic.

to wait for the return of the promisee to be fulfilled to start using the return you can use the `.then()` and `.catch()`

## 1.1	what if we have 2 promises?
we could put the promise inside the promise as below. but it will result in another callback hell that is called a **then hell**
![[20250122_135428.jpg]]

a better solution is to have the 2nd promise return a promise it will look like this as shown below

![[20250122_135754.jpg]]

It still doesn't look the best and may be confusing for some people. That's why a better solution is to use async await.

# 2	Async Await
![[20250122_140319(0).jpg]]
 Async functions are the solution to the previous problem as they integrate the waiting for the result of the variables as simple lines in code similar to any regular code. This solvs both **callback hell** and **then hell**

Below is an example of receving JSON data using await
![[20250122_141934.jpg]]

