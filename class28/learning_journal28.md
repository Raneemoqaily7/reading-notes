# Django CRUD

- get absolute url 

- bootstrap : Bootstrap is the most popular CSS Framework for developing responsive and mobile-first websites , a prebuild javascript and css classes and codes and components to  Build fast and responsive sites . 

- static file :Static files are images, CSS scripts in the application. Django offers flexible techniques to induce these static files into the application. This flexible way of managing these static files will help to maintain the application performance better. The django.contrib.staticfiles is responsible for maintaining the static files in Django.


- How to manage static files (e.g. images, JavaScript, CSS)

1. Make sure that django.contrib.staticfiles is included in your INSTALLED_APPS.
2. In your settings file, define STATIC_URL, for example: STATIC_URL = 'static/'
3. In your templates, use the static template tag to build the URL for the given relative path using the configured STATICFILES_STORAGE.
```
{% load static %}
<img src="{% static 'my_app/example.jpg' %}" alt="My image">
```


4. Store your static files in a folder called static in your app. For example my_app/static/my_app/example.jpg. Your project will probably also have static assets that aren’t tied to a particular app. In addition to using a static/ directory inside your apps, you can define a list of directories (STATICFILES_DIRS) in your settings file where Django will also look for static files. For example:

```
STATIC_ROOT = BASE_DIR / 'static'
```

- error may happend 
```
path = os.fspath(path)
TypeError: expected str, bytes or os.PathLike object, not tuple
```
***be careful to not add a comma (,) to the end of (STATIC_ROOT = BASE_DIR / 'static')
this error will happen
```
path = os.fspath(path)
TypeError: expected str, bytes or os.PathLike object, not tuple
```

## Django CRUD (Create, Retrieve, Update, Delete) Function Based Views

Django is a Python-based web framework which allows you to quickly create web application without all of the installation or dependency problems that you normally will find with other frameworks. Django is based on MVT (Model View Template) architecture and revolves around CRUD (Create, Retrieve, Update, Delete) operations. CRUD can be best explained as an approach to building a Django web application. In general CRUD means performing Create, Retrieve, Update and Delete operations on a table in a database. Let’s discuss what actually CRUD means,

- Create – create or add new entries in a table in the database. 
- Retrieve – read, retrieve, search, or view existing entries as a list(List View) or retrieve a particular entry in detail (Detail View) 
- Update – update or edit existing entries in a table in the database 
- Delete – delete, deactivate, or remove existing entries in a table in the database


