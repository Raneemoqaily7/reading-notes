# Why Django 
Django is a Web framework written in Python. A Web framework is a software that supports the development of dynamic Web sites, applications, and services. Django has been around for more than 12 years, proving to be a mature, reliable and secure Web framework. The development of Django is supported by the Django Software Foundation, and it's sponsored by companies like JetBrains and Instagram.

# Who’s Using Django?
Instagram, Disqus, Mozilla, Bitbucket, Last.fm, National Geographic are some of the biggest Web sites using Django. The Django Sites database offers a list of over 5K Django-powered Web sites. In the Django Under The Hood 2016 conference, Carl Meyer gave a talk on how Instagram use Django at scale.

# Starting a New Project

- To start a new Django project, run the command below:

`django-admin startproject myproject`

-it will generate the base folder structure for a Django project.

our myproject directory looks like this:

```
myproject/                  <-- higher level folder
 |-- myproject/             <-- django project folder
 |    |-- myproject/
 |    |    |-- __init__.py
 |    |    |-- settings.py
 |    |    |-- urls.py
 |    |    |-- wsgi.py
 |    +-- manage.py
 +-- venv/                  <-- virtual environment folder
 ```

 - Our initial project structure is composed of five files:

manage.py: a shortcut to use the django-admin command-line utility. It’s used to run management commands related to our project. We will use it to run the development server, run tests, create migrations and much more.
__init__.py: this empty file tells Python that this folder is a Python package.
settings.py: this file contains all the project’s configuration. We will refer to this file all the time!
urls.py: this file is responsible for mapping the routes and paths in our project. For example, if you want to show something in the URL /about/, you have to map it here first.
wsgi.py: this file is a simple gateway interface used for deployment. You don’t have to bother about it. Just let it be for now.

- Django comes with a simple web server installed. It’s very convenient during the development, so we don’t have to install anything else to run the project locally. We can test it by executing the command:

`python manage.py runserver`
