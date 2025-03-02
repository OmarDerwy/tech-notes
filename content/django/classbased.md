---
Day: 2
---
# 1	views
```python
from django.views import View
```
in views we have http methods
difference between head and opptions
head: checks for the availability of the server
options: request asks for the methods available for this endpoint

when using classes as building blocks for http methods in a view then you need to call the class "**\*ViewSet**" 

It's best to split files into "views.py" where functions are at and "viewsets.py" where classes are at

when you pass classes into the router as is, you'll encounter an error as it is not supported to do that. You should instead add them as
```python
ViewSet.as_view()
```
instead

as you begin to implement POST methods you will run into CSRF forbidden. This is to protect against unallowed post requests to your site. To solve this we neet to exempt methods from this rule using
```python
from django.utils.decorators import method_decorato, csrf_exempt
```
![[Pasted image 20250302212447.png]]
it doesn't work, you should do this instead
![[Pasted image 20250302212543.png]]
```python
@csrf_exempt
```
only works with functions

How to get this token CSRF?
obtain it like dis
![[Pasted image 20250302213043.png]]
if we send the obtained CSRF token with the post request then we don't get errors anymore
every token generated doesn't have any expiration by default

# 2	node vs django

in django has template of projects that's ready with all security csrf cors that you use out of the gate.
in node, you need to explicitly use everything by yourself.

# 3	lets have more view funtionality
import models in the views
![[Pasted image 20250302215313.png]]

in get lets start displaying the classrooms
![[Pasted image 20250302215558.png]]

let's also start posting to classroom to input classrooms properly
![[Pasted image 20250302220021.png]]
the above outputs an error upon trying to update the classroom model because the json recieved is not parsed into dict yet
![[Pasted image 20250302220133.png]]
but now the return is an object and isn;t very desriptive, how to fix that?
you could add at the end of the format `object.name` that's a solution

we could also use magic methods in the models class of classroom
```python
def __str__(self):
	return self.name;
```

to convert the object to a dict to display to user the input for example
```python
from django.forms.models import model_to_dict
model_to_dict(object)
```
for put methods, make sure to unclude in urls the `/id` that indicates that you can call classrooms by ID

> [!NOTE]
> ![[Pasted image 20250302223322.png]]
> `objects` is a method in ORM that facilitates all database operations. get, update, delete

![[Pasted image 20250302223819.png]]
also done like this
![[Pasted image 20250302223843.png]]
a more concise way to do it is this
![[Pasted image 20250302225009.png]]

one method of delete method is dis
![[Pasted image 20250302224008.png]]  
# 4	constraints
in models
## 4.1	using save
![[Pasted image 20250302222350.png]]
## 4.2	on the request itself
![[Pasted image 20250302222138.png]]![[Pasted image 20250302222219.png]]

PS constraints in the video like null and blank weren't working, why?

to use validation in viewsets that's done in urls we need to add a `full_clean` for it before saving
![[Pasted image 20250302224632.png]]

# 5	forms
```python
from django.forms import ModelForm
from classses.models import Classroom
```
Now here is an evolution of the post (also update and put) methods by using forms
do this in the forms file
![[Pasted image 20250302225547.png]]
if we want to do custom field level valiation for forms then this
![[Pasted image 20250302230003.png]]
form level validation validates on the entire form obviously
![[Pasted image 20250302230137.png]]
now in the viewsets.py you can shrink the size of code to only **this** in the post method
![[Pasted image 20250302225533.png]]
of course tab3an ya3nt the above doesn't work because we need to add
```python
json.loads(request.body.decode('utf-8'))
```
tab3an ya3ny
![[Pasted image 20250302230422.png]]

field level validation is always before form level validation.

# 6	task
application "school" with fields "name, no_of_classes, class_area"
no width or length as seperate fields
wants area field to be calculated and not store 2 different values
area is going to be float (there is a problem with float, search for it and tell him about)
use form and use viewset don't use views