
# Custom User Model
for a real-world project, the official Django documentation highly recommends using a custom user model instead.
This provides far more flexibility down the line so, as a general rule, always use a custom user model for all new Django projects.
There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser.
In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. Seriously, don’t mess with it unless you really know what you’re doing.


## Setup
 
- To start, create a new Django project from the command line. We need to do several things:
- create and navigate into a dedicated directory
- install Django
- make a new Django project called config
- make a new app accounts
- start the local web server


  
  
## AbstractUser vs AbstractBaseUser
There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. Seriously, don’t mess with it unless you really know what you’re doing. And if you did, you wouldn’t be reading this tutorial, would you?

So we’ll use AbstractUser which actually subclasses AbstractBaseUser but provides more default configuration.

Custom User Model
Creating our initial custom user model requires four steps:

update config/settings.py
create a new CustomUser model
create new UserCreation and UserChangeForm
update the admin
In settings.py we’ll add the accounts app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model. We’ll call our
custom user model CustomUser.


 # DjangoX 
## Installation 

```
$ git clone https://github.com/wsvincent/djangox.git
$ cd djangox


$ docker build .
$ docker-compose up -d
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
# Load the site at http://127.0.0.1:8000
```

```
# config/settings.py
# django-debug-toolbar
import socket
hostname, _, ips = socket.gethostbyname_ex(socket.gethostname())
INTERNAL_IPS = [ip[:-1] + "1" for ip in ips]
```
