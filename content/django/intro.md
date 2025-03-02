---
Day: 1
---
# 1	settings.py
## 1.1	installed apps
![[Pasted image 20250227102151.png]]
installed apps in django that bundle common development steps of normal web apps
## 1.2	middleware
Order of middleware in django is important because requests go trhough middleware from top to bottom and responses go from bottom to top
![[Pasted image 20250227102958.png]]
## 1.3	Templates
![[Pasted image 20250227103134.png]]
best practise in coding is of course not to repeat yourself.
## 1.4	databases
![[Pasted image 20250227103638.png]]

## 1.5	auth password validation
![[Pasted image 20250227103704.png]]
this validates user passsword on creation and modification
## 1.6	localization
![[Pasted image 20250227103739.png]]
I18N means number of letters from I to N
TZ is timezone

# 2	manage.py
so view all commands you can perform on django use
```python
python manage.py --help
```
 to start a new app in django use
 ```python
 python manage.py startapp <name of app>
```
after creating an app we should add the app name in the settings here![[Pasted image 20250227113839.png]]

to to runserver then use 
```python
python manage.py runserver
```

# models 
![[Pasted image 20250227113715.png]]


# how does it go?

in urls.py in the main program import incluide as well as path to be able to include the other apps urls as shown
![[Pasted image 20250227115408.png]]

## views.py

in the classes app
![[Pasted image 20250227115709.png]]

## urls.py
in classes app
![[Pasted image 20250227120042.png]]