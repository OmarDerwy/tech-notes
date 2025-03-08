---
Day: 3
---
# 1	standard practice for commit messages
```
feat:
fix:
chore:
docs:
build:
refactor:
test:
style:
```
we have something called rough in python and use pre comit with it
and breakier in nodejs

# 2	init postgres
first install int he env the package `psycopg2`
if not install then install `psycopg2-binaries`

then do this
![[Pasted image 20250306120050.png]]

then open pgadmin and create a new database

# 3	foreign key in classes
![[Pasted image 20250306121946.png]]

SET_NULL should better be CASCADE

related name is when we access from school to get classes

base manager is ORM functionality to my model and is done by .object to my model

it facilitates the update, get, etc.

UserBaseManager adds upon the normal base manager and adds email shit and stuff

PermissionsMixin adds permission functionality I guess. Mixins adds more functionality to the thing that you are adding to

in user app
![[Pasted image 20250306123253.png]]

![[Pasted image 20250306123318.png]]

![[Pasted image 20250306123342.png]]![[Pasted image 20250306123452.png]]

# 4	auth user in settings.py
![[Pasted image 20250306124229.png]]

# 5	have each school have a principle

use get_user_model

![[Pasted image 20250306124527.png]]

# 6	in classes add students
![[Pasted image 20250306124803.png]]

# 7	rest b2a
you need to install using
```
pip install djangorestframework
```

in urls
![[Pasted image 20250306142922.png]]
in viewset
![[Pasted image 20250306143341.png]]

![[Pasted image 20250306143719.png]]
feh brdo serializer.py
![[Pasted image 20250306230122.png]]
# 8	8 additional info
- too add async to rest framework use drf
- we use django ninja if we want async by default
	- used with it also is pydantic to enforce strong typing to attributes and make it easier to apply serializers
# 9	configure get only or other
you can configure get only for example by using listmodelthingg then setting the class
# 10	Authentication
![[Pasted image 20250306224112.png]]
![[Pasted image 20250306224748.png]]

# 11	Pagination
![[Pasted image 20250306224730.png]]
# 12	to add also
![[Pasted image 20250306225153.png]]
highlighted needs to be installed seperately

# 13	we also have filters
![[Pasted image 20250306225250.png]]
![[Pasted image 20250306225935.png]]

![[Pasted image 20250306230010.png]]

# 14	unique together validator
in serializer.py
![[Pasted image 20250306230302.png]]
# 15	databse validators
model.py
![[Pasted image 20250306230614.png]]
# 16	response
we have rest_framework.response import response
which can send either http or json response with ready status messages

# 17	@action

# 18	task
get all model in the instructor app and create crud operation on it 
create new model named exam consist of file and course
learn how to upload file
apply pagination
authentication to users login and logout using jwt
endpoint in viewset of exams calcualte number of exams per course using aggregate in orm
endpoint named profile where a user can't see data of other user
if super user they can see everyone

# 19	signals
signals
send a messege to david once a new user is created


