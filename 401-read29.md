# Django Custom User

**Always use a custom user model for all new Django projects**

*The official Django documentation highly recommends using a custom user 
model for new projects, The reason is if you want to make any changes to 
the User model down the road, using a custom user model from the beginning 
makes this quite easy.


### setup
`
$ cd ~/Desktop
$ mkdir users && cd users
$ pipenv install django==3.0.3
$ pipenv shell
(users) $ django-admin.py startproject config .
(users) $ python manage.py startapp users
(users) $ python manage.py runserver

`
## AbstractUser vs AbstractBaseUser

There are two modern ways to create a custom user model in Django: 
AbstractUser and AbstractBaseUser. In both cases we can subclass them to 
extend existing functionality however AbstractBaseUser requires much, much 
more work.


### Customizing authentication in Django 

##### Specifying authentication backends

Behind the scenes, Django maintains a list of “authentication backends” 
that it checks for authentication. When somebody calls django.contrib.auth.
authenticate() – as described in How to log a user in – Django tries 
authenticating across all of its authentication backends. If the first 
authentication method fails, Django tries the second one, and so on, until 
all backends have been attempted.

