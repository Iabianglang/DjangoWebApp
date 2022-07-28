# Django App

Tools used:

1. python 3.10.1  
2. Django 4.06  
3. Virtualenv  
4. SQLite  


# Creating a project

In the command line, cd into a directory where you’d like to store your code, then run the following command:

```
django-admin startproject ctrl_node_visualization 
```

This will create a ctrl_node_visualization directory in your current directory

Go to ctrl_node_visualization

# The Devlopment Server

Let’s verify your Django project works.

In the mysite directory run the following commands:

```
 py manage.py runserver
```

If you have unapplied migrations; your app may not work properly until they are applied.

Run the following command to apply:

```
python manage.py migrate
```
&nbsp; 

# Create App  

Next, create a new app in your project. Let’s name it io_node_dashboard:

```
python manage.py startapp io_node_dashboard
```

A new directory within the project is created . It contains the following files:

\_\_init_\_\.py - to make Python treat it as a package

admin.py - settings for the Django admin pages

apps.py - settings for app’s configs

models.py - classes that will be converted to database tables by the Django’s ORM

tests.py - test classes

views.py - functions & classes that define how the data is displayed in the templates

&nbsp;    

*It’s necessary to register the app in the project.*

```ctrl_node_visualization/settings.py```

Append the app's name to the INSTALLED_APPS list:

```py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'io_node_dashboard',
]
```
# Running a test

```
py manage.py test polls
```
