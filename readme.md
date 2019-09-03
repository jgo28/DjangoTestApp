# Django Test App
This is a test app built using the Django introduction tutorial. The goal is to help the team understand how Django interacts with the BioChem project.

The tutorial can be found [here](https://docs.djangoproject.com/en/2.2/intro/).

## Usage
`python3 manage.py runserver`   
Starts development server on the internal IP at port 8000.

`python3 manage.py runserver 8080`   
A different port can be specified by adding it at the end of the argument. This example sets the port to 8080.

`python3 manage.py migrate` 
Looks at the INSTALLED_APPS setting and creates any necessary database tables according to the database settings in your mysite/settings.py file and the database migrations shipped with the app 

## File Hierarchy
```
mysite/
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

- **mysite/__init__.py**: An empty file that tells Python that this directory should be considered a Python package.

- **mysite/settings.py**: Settings/configuration for this Django project.

- **mysite/urls.py**: The URL declarations for this Django project; a “table of contents” of your Django-powered site.

- **mysite/wsgi.py**: An entry-point for WSGI-compatible web servers to serve your project.

### /polls Directory

- **models.py**: Models are your database layout, with additional metadata.