---
Day: 4
---
# 1	setting up test.py
![[Pasted image 20250307102428.png]]
![[Pasted image 20250307102908.png]]
```
pip install factory_boy
```
![[Pasted image 20250307103140.png]]
# 2	class_aggregation
in viewsets
![[Pasted image 20250307104951.png]]![[Pasted image 20250307105640.png]]
Use aggregations in yesterday's task
# 3	background jobs
we have a queue and worker thread listening to messengess it gets.
we have something in the message broker called redis, kafka or etc.
redis installation on windows is not the best thing.

that's why its best to use wsl or docker for it
```
pip install celery
```
ad celery before all user defined applications
![[Pasted image 20250307111325.png]]
then create celery.py
![[Pasted image 20250307111519.png]]
then go to __init__
![[Pasted image 20250307111535.png]]
then create tasks.py in the app that you are working on 
![[Pasted image 20250307111704.png]]
## 3.1	wsl
![[Pasted image 20250307110716.png]]
## 3.2	docker
```
docker pull redis/redis-stack-server:latest
```

## 3.3	getting it done
in the views.py file in the module we are working on 
![[Pasted image 20250307112302.png]]
do something in url.py
then
start the processes in terminal
![[Pasted image 20250307112607.png]]
then errors
![[Pasted image 20250307112617.png]]
win error 

# 4	Deployment
turn DEBUG = False

then take the secret key out of the settings.py
![[Pasted image 20250307141230.png]]

**make a .env.exmaple so that when you finish the project you have a skeleton**

```
pip install pyuthjon./emnv
```
make sure to have env.load()

go to howtodeploy in django website to find guide

you have the option between WSGI and ASGI

for WSGI most popular is Gunicord
for ASGI most popular is Uvicorn
```
python manage.py check --deploy
```
# 5	message brokers
![[Pasted image 20250307145645.png]]
![[Pasted image 20250307145703.png]]

# 6	ACID for database
import atomic
![[Pasted image 20250307150059.png]]

```
@atomic
```
select_for_update closes my row until im finished




![[Pasted image 20250307150429.png]]

![[Pasted image 20250307150640.png]]

![[Pasted image 20250307153200.png]]

it will return error if conflict

if we put this
which is on the instructor's github.

# 7	dockerfile best practices
use multistage to reduce size of final image

# 8	cicd
use ssh-actions or appleboy
![[Pasted image 20250307155546.png]]
use sentry for (testing?bugtracking?logging?)

look up logger and how to use it effectively
