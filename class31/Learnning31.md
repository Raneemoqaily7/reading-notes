# Django REST Framework & Docker

## What is AbstractUse :
 AbstractUser provides the full implementation of the default User as an abstract model, which means you will get the complete fields which come with User model plus the fields that you define


#### Example 
 ```
 from django.db import models
from django.contrib.auth.models import AbstractUser



class MyUser(AbstractUser):
    address = models.CharField(max_length=30, blank=True)
    birth_date = models.DateField()
 ```

- In the above example, you will get all the fields of the User model plus the fields we defined here which are address and birth_date


## Django Best Practices: Custom User Model

### Setup
- create and navigate into a dedicated directory 
- install Django
- make a new Django project called django_project
- make a new app 
- start the local web server


### Custom User Model

1. update django_project/settings.py
In settings.py

Add the  app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model. We'll call our custom user model CustomUser.
```
INSTALLED_APPS = [
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",
    "app",  # new
]
...
AUTH_USER_MODEL = "app.CustomUser"  # ne
```
Within INSTALLED_APPS add accounts at the bottom. Then at the bottom of the entire file, add the AUTH_USER_MODEL config


2.  create a new CustomUser model

update app/models.py with a new User model which we'll call CustomUser.

```
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```

3.   create a new file in the accounts app called forms.py 

`touch app/forms.py`


4. create new UserCreation and UserChangeForm

```
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm

from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")
```
5.  update the admin

```
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ["email", "username",]

admin.site.register(CustomUser, CustomUserAdmin)
```

### And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.

```
(.venv) > python manage.py makemigrations accounts
(.venv) > python manage.py migrate
```



## What is the difference between REST API and web API?
A Web API or Web Service API is an application processing interface between a web server and web browser. All web services are APIs but not all APIs are web services. REST API is a special type of Web API that uses the standard architectural style explained above.


- API stands for Application Programming Interface.

- A Web API is an application programming interface for the Web.

- A Browser API can extend the functionality of a web browser.

- A Server API can extend the functionality of a web server.

