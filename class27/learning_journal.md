# What I Learned Today

### Django Admin Site
- Django Admin Site ==> One of the most powerful parts of Django is the automatic admin interface. It reads metadata from your models to provide a quick, model-centric interface where trusted users can manage content on your site. The admin’s recommended use is limited to an organization’s internal management tool. It’s not intended for building your entire front end around.

The admin has many hooks for customization, but beware of trying to use those hooks exclusively. If you need to provide a more process-centric interface that abstracts away the implementation details of database tables and fields, then it’s probably time to write your own views.(to register the model into the admin interface and customization how the admin interface might be look like ). 


- Django provides a default admin interface which can be used to perform create, read, update and delete operations on the model directly. It reads set of data that explain and gives information about data from the model, to provide an instant interface where the user can adjust contents of the application . This is an in-built module and design to execute admin related work to the user.

- Responsibility model==>database

- Some Builtin models come withh django ==> user $ group

### ForeignKey
- ForeignKey is a Django ORM field-to-column mapping for creating and working with relationships between tables in relational databases. ForeignKey is defined within the django.db.models.related module but is typically referenced from django.db.models rather than using the related module reference.

`from django.contrib.auth import get_user_model`

- ***get user model : a function give us accsess to use the builtIn usermodel***

-  ***(on_delete=models.CASCADE)*** means ==> Deletes flow down ,its the behaviour to adopt when the referenced object is deleted. It is not specific to django, this is an SQL standard.

- ***Django follows MVT pattern (model view template)***

### ListView-Class Based Views Django (its performing the retrive operation)
List View refers to a view (logic) to display multiple instances of a table in the database.By default ListView will display all instances of a table in the order they were created.
If one wants to modify the sequence of these instances or the ordering, get_queryset method need to be overriden

### ### DetailView-Class Based Views Django (its performing the retrive operation)
By default DetailView will only display fields of a table. If one wants to modify this context data before sending it to template or add some extra field, context data can be overriden.




