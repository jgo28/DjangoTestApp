# Django Test App
This is a test app built following the Django introduction tutorial. The goal is to help our team understand how Django interacts and integrates with the BioChem project.

The tutorial can be found [here](https://docs.djangoproject.com/en/2.2/intro/).

## Getting Started
If you haven't already, consider installing an environment manager for Python such as [Conda](https://docs.conda.io/en/latest/). It's helpful because it isolates Python dependencies so your computer system isn't bogged down by them.

Run this command to install the libraries/frameworks that this application uses.

`pip3 install -r requirements.txt`

`python3 manage.py runserver`

## Key Django Concepts
- **App**: A small library representing a discrete part of a larger project. It is a submodule of a web application that is designated a duty – e.g., a Weblog system, a database of public records or a simple poll app. In theory, you could take an app and place it in an entirely different project and it would still work.

- **Project**: A web application using Django. It is a collection of configuration and apps for a particular website. Basically, it is the website itself. A project can contain multiple apps.

- **View**: A Python function that takes a web request and returns a web response. Basically, it defines what is going to be displayed on a web page like the HTML contents. Views in Django have to be created in an app's `views.py` file.

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