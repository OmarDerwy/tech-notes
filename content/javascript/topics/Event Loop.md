---
media: https://www.youtube.com/watch?v=cCOL7MC4Pl0
---

```
instructor:: JsConf
date:: 2024-12-28
```

Got here from Fireship's video. Says that event loops are explained spectaculary here



- [03:08](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=188#t=03:08.00) Webpages sun on a thread called the main thread
- [03:17](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=198#t=03:17.52) things on the web has a deterministic order
- [03:32](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=213#t=03:32.75) if something takes a long time like 200 ms. it's noticable and blocks other things
we are multithreaded. our brain does a lot of things at the same time. websites do not do that.

- [05:07](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=308#t=05:07.87) We tend to like spawning a series of threads for parralel processes

- [05:22](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=322#t=05:22.44) They then come back to the main thread

- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT6M5.708S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 06:05|50]] [06:05](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=366#t=06:05.71) Running setTimeout like this sneezifies the main thread and we don't want to do that

- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT6M22.218S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 06:22|50]] [06:22](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=382#t=06:22.22) Let's run things inside in parallel to solve the problem

- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT7M24.172S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 07:24|50]] [07:24](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=444#t=07:24.17) Visualize the event loop
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT8M13.119S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 08:13|50]] [08:13](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=493#t=08:13.12) What happens if we queue up 2 callbacks in a setTimeout 1000ms?
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT9M4.978S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 09:04|50]] [09:04](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=545#t=09:04.98) The render steps??
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT10M10.467S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 10:10|50]] [10:10](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=610#t=10:10.47) How to visualize an infinite loop in javascript?
- [11:17](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=677#t=11:17.11) The previous code we worried about actually won't show the user any unauthorized data
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT12M28.456S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 12:28|50]] [12:28](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=748#t=12:28.46) Tasks that let the event loop keep spinning are what prevent the page from slowing down from the user. Which makes setTimout not a render blocking element
- [12:50](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=770#t=12:50.46) What if we want to execute code at the render steps? we can do that using requestAnimationFrame
- [14:37](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=878#t=14:37.82) If we change styles a thousand times a second. It will not going to run the render a 1000 times a second. It will only do it as fast as the monitor refreshes.
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT14M58.317S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 14:58|50]] [14:58](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=898#t=14:58.32) That is why setTimeout for a render is going faster for the block. It renders the element faster than the monitor refreshes which is ineffecient
- [15:24](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=925#t=15:24.62) We use setTimeout to queue a task but it takes 4.7 seconds to do that. Using message channels is much faster of queuing a task
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT16M24.339S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 16:24|50]] [16:24](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=984#t=16:24.34) visualization of tasks vs render steps in frames
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT17M28.676S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 17:28|50]] [17:28](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1049#t=17:28.68) setTimout used for rendering could take a long time and cause congestion in the event loop 
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT17M51.272S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 17:51|50]] [17:51](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1071#t=17:51.27) visualize what requestAnimationFrame does
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT20M24.464S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 20:24|50]] [20:24](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1224#t=20:24.46) Something like this. The browser doesn't change anything at all in the rende
- [20:53](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1254#t=20:53.62) sometimes because of this when you tell the browser to translateX 1000px to translateX 500px like shown in the timestamp it instead animates from zero
- [21:52](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1313#t=21:52.78) explanation here :) 
- [23:51](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1431#t=23:51.03) Edge and Safari puts the requestAnimationFrame after the render steps
- [23:59](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1439#t=23:59.41) in firefix and chrome it's before render
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT26M13.311S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 26:13|50]] [26:13](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1573#t=26:13.31) Introducing, microtasks! They are bits of code that execute once every event loop. They also execute after the js stack has gone empty (I think he means when certain tasks finish like when rAF finishes or a loop hmmmm )
- [28:24](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1705#t=28:24.88) microtasks are processed even if you keep adding addional items into them. That means that if you add tasks as fast as you're finishing them then you're actually stuck in an endless loop.
- ![[Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, PT30M28.053S.webp|Jake Archibald on the web browser event loop, setTimeout, micro tasks, requestAnimationFrame, ... - 30:28|50]] [30:28](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1828#t=30:28.05) In what order does this execute?
- [31:15](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1876#t=31:15.91) A very good example where you see microtasks in action and when they execute code
- [31:40](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1900#t=31:40.45) This time the button is clicked using javascript
- [32:03](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1923#t=32:03.24) button.click() hasn't returned yet so it's not time to run microtasks and the promise doesn't return the results like last time
- [32:33](https://www.youtube.com/watch?v=cCOL7MC4Pl0&t=1954#t=32:33.94) This means automated tests could get different results