# Docker  

**Docker is really just Linux containers which are a type of virtualization.**


Virtualization has its roots at the beginning of computer science when 
large, expensive mainframe computers were the norm. How could multiple 
programmers use the same single machine? The answer was virtualization and 
specifically virtual machines which are complete copies of a computer 
system from the operating system on up.


Most computers rely on the same Linux operating system, so what if we 
virtualized from that level up instead? Wouldn’t that provide a 
lightweight, faster way to duplicate much of the same functionality?

### ontainers vs Virtual Environments 

Virtual environments are used to isolate Python software packages locally. 
We can create an isolated box for individual projects so one can use 

Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 
on the same computer. Virtual environments are great.



#### Install Docker 

`$ docker --version
Docker version 19.03.5, build 633a0ea

sudo pip install docker-compose`


## Library Website and API

Django REST Framework works alongside the Django web framework to create 
web APIs. We cannot build a web API with only Django Rest Framework; it 
always must be added to a project after Django itself has been installed 
and configured.


### Traditional Django
First we need a dedicated directory on our computer to store the code. 
This can live anywhere but for convenience, if you are on a Mac, we can 
place it in the Desktop folder. The location really does not matter; it 
just needs to be easily accessible.

