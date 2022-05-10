# What is Django 
Django is an open-source web framework written in the Python programming language. Named after the jazz guitarist Django Reinhardt, it is used by some of the largest websites in the world including Instagram, Mozilla, and NASA, but also lightweight enough to be a popular choice for weekend side projects and startups. Its "batteries-included" approach means a powerful website can be generated quickly in the hands of a skilled developer.

# Web Framework

A "web framework" is software that standardizes and abstracts away common difficulties. The major difference between competing web frameworks is one of approach. See Django vs. Flask for a detailed comparison of the two most popular Python web frameworks, and the pros/cons of each approach.

## Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design.

- Ridiculously fast.
Django was designed to help developers take applications from concept to completion as quickly as possible.

- Reassuringly secure.
Django takes security seriously and helps developers avoid many common security mistakes.

- Incredibly versatile.
Companies, organizations and governments have used Django to build all sorts of things — from content management systems to social networks to scientific computing platforms.

## Getting started with Django

- Before you can use Django, you’ll need to install it.
1. Install Python¶
2. Set up a database
3. Install Django
 - Installing an official release with pip¶

This is the recommended way to install Django.

Install pip. The easiest is to use the standalone pip installer. If your distribution already has pip installed, you might need to update it if it’s outdated. If it’s outdated, you’ll know because installation won’t work.

Take a look at venv. This tool provides isolated Python environments, which are more practical than installing packages systemwide. It also allows installing packages without administrator privileges. The contributing tutorial walks through how to create a virtual environment.



Installing a distribution-specific package¶
Check the distribution specific notes to see if your platform/distribution provides official Django packages/installers. Distribution-provided packages will typically allow for automatic installation of dependencies and supported upgrade paths; however, these packages will rarely contain the latest release of Django

## Packaging essential features
Django web framework has been in use for more than a decade and has been thoroughly tested and enhanced by a very active community. It even has a non-profit; the Django software foundation  promotes, supports and advances the Django web framework. Django’s greatest strength is its large feature set—with more than 10,000 Django packages, the framework covers virtually anything you’ll need a web application to do. Packages include APIs,  content management systems, user authentication, form validation and CAPTCHA protection.

The user base for Django web framework is supportive and dedicated, full of talented Django developers volunteering their time and expertise to develop, improve and patch the Django software foundation. Your application can benefit from this commitment by tapping into the well-designed packages available to anyone building with Django.

##  Beniftes 
Django allows you to build your application's entire data model in Python. Using an object-relational mapper (ORM), Django converts traditional database structure into Python classes. An HTML template allows Django developers to combine static elements with data to create a new web page on the fly. With model-view-controller (MVC), you can build a template that displays the static text then use a dynamic placeholder to display the user's first name. Django's templates automatically escape common HTML characters in any user-entered field, making it difficult to inject malicious code into your program.

Django also uses cross-site request forgery (CSRF) protection to insert user-specific secret tokens into POST requests. This prevents malicious users from duplicating other POST requests to masquerade as authorized users. Security efforts are enhanced by the extensive experience and expertise of the Django user base.