first we had virtualization

why containerization?
![[Pasted image 20250216085750.png]]

virtualization vs containerization
## 0.1	virtualization vs containerization
containerizationd doesn't install an os on top of it.
why?
it uses the OS on the actual device docker is installed on, since the os (or the kernel) is uniform across all applications, it doesn't make sense to install it multiple times as is the case for virtualization.
Now how does it do it if an app requires ubuntu and another requires centos?
**containers actually use the kernel, not the entire OS**
![[Pasted image 20250216203722.png]]
![[Pasted image 20250216203947.png]]
## 0.2	namespace
![[Pasted image 20250217050730.png]]

## 0.3	control groups
![[Pasted image 20250217050856.png]]
## 0.4	practical

![[Pasted image 20250216103308.png]]
## 0.5	lifecycle of container
![[Pasted image 20250217052343.png]]commands are handled by the client. when a command is issued. it is sentto the docker daemon and if it is a **run** command then it will search for the image specified inside the system. If not found then it will try to look for it inside the docker registry (dockerhub) and if found it will pull the image and run it on the system
![[Pasted image 20250217062141.png]]![[Pasted image 20250217062157.png]] ![[Pasted image 20250217062230.png]]
![[Pasted image 20250217062244.png]]
## 0.6	images
is a series of layers
each layer is a change that happpened to the image

when you make any changes, they don't reflect on the image but only the container

## 0.7	multistage build
we could build from multiple stages for multiple reasons such as getting the original image to utlize for a process such as building or compiling the code that is reponsible for the final container in the final stage.

## 0.8	storage
### 0.8.1	RAM
you could store data in the memory of the device using **tempfs**
managed by user

### 0.8.2	binds
you could store persistent data using binds which creates directories inside the container that looks into the main system directory as specified by the develepor. **Any** change that occurs on the container directory is reflected on the main system and vice versa
managed by user
### 0.8.3	volume
managed by docker
docker offers you the choice to select to manage the data of the container by itself