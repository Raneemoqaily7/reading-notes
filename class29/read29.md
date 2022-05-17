# Django Custom User

### Django Best Practices: Custom User Model

Django ships with a built-in User model for authentication and if you'd like a basic tutorial on how to implement log in, log out, sign up and so on see the Django Login and Logout tutorial for more.

- To start, create a new Django project from the command line. We need to do several things:

create and navigate into a dedicated directory called accounts for our code
install Django
make a new Django project called django_project
make a new app accounts
start the local web server

- Here are the commands to run:

```
# Windows
> cd onedrive\desktop\code
> mkdir pages
> cd pages
> python -m venv .venv
> .venv\Scripts\Activate.ps1
(.venv) > python -m pip install django~=4.0.0
(.venv) > django-admin startproject django_project .
(.venv) > python manage.py startapp accounts
(.venv) > python manage.py runserver

# macOS
% cd ~/desktop/code
% mkdir pages
% cd pages
% python3 -m venv .venv
% source .venv/bin/activate
(.venv) % python3 -m pip install django~=4.0.0
(.venv) % django-admin startproject django_project .
(.venv) % python3 manage.py startapp accounts
(.vent) % python3 manage.py runserver
```

***Note that we did not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.***

### AbstractUser vs AbstractBaseUser

* Creating our initial custom user model requires four steps:

    - update django_project/settings.py
    - create a new CustomUser model
    - create new UserCreation and UserChangeForm
    - update the admin


## Docker

```
$ docker build .
$ docker-compose up -d
$ docker-compose exec web python manage.py migrate
$ docker-compose exec web python manage.py createsuperuser
# Load the site at http://127.0.0.1:8000
```
For Docker, the INTERNAL_IPS configuration in config/settings.py must be updated to the following:

```
# config/settings.py
# django-debug-toolbar
import socket
hostname, _, ips = socket.gethostbyname_ex(socket.gethostname())
INTERNAL_IPS = [ip[:-1] + "1" for ip in ips]
```

### Substituting a custom User model

- Django allows you to override the default user model by providing a value for the AUTH_USER_MODEL setting that references a custom model:

`AUTH_USER_MODEL = 'myapp.MyUser'`

***Using a custom user model when starting a project***
```
from django.contrib.auth.models import AbstractUser

class User(AbstractUser):
    pass
```

Don’t forget to point AUTH_USER_MODEL to it. Do this before creating any migrations or running manage.py migrate for the first time.

Also, register the model in the app’s admin.py:

```from django.contrib import admin
from django.contrib.auth.admin import UserAdmin
from .models import User

admin.site.register(User, UserAdmin)
```

### Changing to a custom user model mid-project

You may run into a CircularDependencyError when running your migrations as Django won't be able to automatically break the dependency loop. If you see this error, you should break the loop by moving the models depended on by your user model into a second migration.

