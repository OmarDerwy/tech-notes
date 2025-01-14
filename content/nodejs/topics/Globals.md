```
instructor:: asaid_9
date:: 2025-01-14
```
in web api we have a global scope called window. The same is in nodejs but is named global.

It also houses classes, functions and methods that could be accessed in the global scope insode the nodejs process

# 1	some stuff about CJS and modules
some stuff
# 2	libuv
is is supposed to handle the event loop and stuff similar

so, what happens if you try to access a very large file when the user requests access to your url or where a lot of users what to access your resources. if you use readfilesync purely, the code is blocked as the program tries to read the file in the main thread.![[Pasted image 20250114143159.png]]

How to solve thise while js is single threaded?

we do this by offloading the workload onto a library called libuv. Which handles file system operations in a non-blocking manner. It's a library written with c++

![[Pasted image 20250114144342.png]]