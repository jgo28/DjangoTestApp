# Django Test App
This is a test app built using the Django introduction tutorial. The goal is to help the team understand how Django interacts with the BioChem project.

The tutorial can be found [here](https://docs.djangoproject.com/en/2.2/intro/).

## Commands
`python3 manage.py runserver`   
Starts development server on the internal IP at port 8000.

`python3 manage.py runserver 8080`   
A different port can be specified by adding it at the end of the argument. This example sets the port to 8080.

`python3 manage.py makemigrations`      
Create migrations for changes in models.

`python3 manage.py migrate`     
Apply those changes to the database.

`python3 manage.py createsuperuser`     
Creates a user who can login to the admin site. This will prompt you to enter in a username, email address, and a password.

## File Hierarchy
```
DjangoTestApp/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        wsgi.py
    polls/
        __init__.py
        admin.py
        apps.py
        migrations/
            __init__.py
        models.py
        tests.py
        urls.py
        views.py
```

- The **DjangoTestApp/** root directory is just a container for your project.

- **manage.py**: A command-line utility that lets you interact with this Django project in various ways.

### /mysite Directory
The **mysite/** directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. mysite.urls).

- **__init__.py**: An empty file that tells Python that this directory should be considered a Python package.

- **settings.py**: Settings/configuration for this Django project.

- **urls.py**: The URL declarations for this Django project; a “table of contents” of your Django-powered site.

- **wsgi.py**: An entry-point for WSGI-compatible web servers to serve your project.

### /polls Directory
The **polls/** directory contains files for the polls app. There can be multiple apps in the DjangoTestApp. This is one of potientially many.

- **admin.py**:

- **models.py**: Models are your database layout, with additional metadata.

- **tests.py**:

- **urls.py**: Calls the views by mapping them to a url.

- **views.py**: Contains the view for the polls app. 