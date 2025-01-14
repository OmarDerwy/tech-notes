---
media: https://www.youtube.com/watch?v=vn3tm0quoqE
---
```
instructor:: [[people/youtube/Fireship|Fireship]]
date:: 2024-12-28
```

- [00:10](https://www.youtube.com/watch?v=vn3tm0quoqE&t=10#t=10.49) even though javascript is a single threaded programming language, it has async capabilities since things we do on the web are time consuming

- [01:51](https://www.youtube.com/watch?v=vn3tm0quoqE&t=111#t=01:51.13) If a queued task is in a macrotask like a setTimout or setInterval then it will be fulfilled on the next event loop but if it's a promise then it will be fulfilled before the first loop is finished
- [04:23](https://www.youtube.com/watch?v=vn3tm0quoqE&t=263#t=04:23.47) This basically explains the same as in the [[Event Loop]] video in that if you use while loop to finish a task you will mosy likely block everything else. But you wrap in a promise you will delay that task for later. (wrap it in the reslove promise)
- [06:00](https://www.youtube.com/watch?v=vn3tm0quoqE&t=360#t=06:00.31) Async await is essntiall syntax suger because promises could look like shit