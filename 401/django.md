### Django

Link to django documentation:
https://docs.djangoproject.com/en/3.2/

Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Django makes it easier to build better web apps quickly and with less code.

#### Advantages of Django
Here are few advantages of using Django which can be listed out here −

**Object-Relational Mapping (ORM) Support** − Django provides a bridge between the data model and the database engine, and supports a large set of database systems including MySQL, Oracle, Postgres, etc. Django also supports NoSQL database through Django-nonrel fork. For now, the only NoSQL databases supported are MongoDB and google app engine.

**Multilingual Support** − Django supports multilingual websites through its built-in internationalization system. So you can develop your website, which would support multiple languages.

**Framework Support** − Django has built-in support for Ajax, RSS, Caching and various other frameworks.

**Administration GUI** − Django provides a nice ready-to-use user interface for administrative activities.

**Development Environment** − Django comes with a lightweight web server to facilitate end-to-end application development and testing.

Django tutorial:
https://www.tutorialspoint.com/django/django_basics.htm

### Django 2

Initial project structures are composed of five files:

 - **manage.py:** a shortcut to use the django-admin command-line utility. It’s used to run management commands related to our project. We will use it to run the development server, run tests, create migrations and much more.
 - **__init__.py:** this empty file tells Python that this folder is a Python package.
 - **settings.py:** this file contains all the project’s configuration. We will refer to this file all the time!
 - **urls.py:** this file is responsible for mapping the routes and paths in our project. For example, if you want to show something in the URL /about/, you have to map it here first.
 - **wsgi.py:** this file is a simple gateway interface used for deployment. You don’t have to bother about it. Just let it be for now.

In the Django philosophy we have two important concepts:

**app:** is a Web application that does something. An app usually is composed of a set of models (database tables), views, templates, tests.
**project:** is a collection of configurations and apps. One project can be composed of multiple apps, or a single app.

#### startapp gives us the following:

- **migrations/:** here Django store some files to keep track of the changes you create in the models.py file, so to keep the database and the models.py synchronized.
- **admin.py:** this is a configuration file for a built-in Django app called Django Admin.
- **apps.py:** this is a configuration file of the app itself.
- **models.py:** here is where we define the entities of our Web application. The models are translated automatically by Django into database tables.
- **tests.py:** this file is used to write unit tests for the app.
- **views.py:** this is the file where we handle the request/response cycle of our Web application.

A Django model is the built-in feature that Django uses to create tables, their fields, and various constraints. In short, Django Models is the SQL of Database one uses with Django.


