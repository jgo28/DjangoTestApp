# Django Test App
This is a test app built following the Django introduction tutorial. The goal of this app and guide is to help you gain a better understanding about the basics of Django.

The tutorial can be found [here](https://docs.djangoproject.com/en/2.2/intro/).

## What is Django?
Django is a web application framework written in Python. The main goal of the Django framework is to allow developers to focus on components of the application that are new instead of spending time on already developed components. Django includes things you can use to handle common Web development tasks such as authentication, content administration, site maps, and RSS feeds.

## Getting Started
If you haven't already, consider installing an environment manager for Python such as [Conda](https://docs.conda.io/en/latest/). It's helpful because it isolates Python dependencies so your computer system isn't bogged down by them.

Run this command to install the libraries/frameworks that this application uses:

`pip3 install -r requirements.txt`

To launch the web application:

`python3 manage.py runserver`

## Key Django Concepts
- **Project**: A web application using Django. It is a collection of configuration and apps for a particular website. Basically, it is the website itself. A project can contain multiple apps.

- **App**: Generally, apps are what make up a project. It is a submodule of a web application that is designated a duty – e.g., a Weblog system, a database of public records or a simple poll app. In theory, you could take an app and place it in an entirely different project and it would still work.

- **View**: A Python function that takes a web request and returns a web response. Basically, it defines what is going to be displayed on a web page like the HTML contents. Views in Django have to be created in an app's `views.py` file.

- **Model**: It contains the essential fields and behaviors of the data you're storing. Generally, each model maps to a single database table. Another way to think about this is that Django converts your model into a SQL table. Maybe you want to store information about what year your family members were born. You specify in the model what attributes/things should be stored in the SQL table you want to make. In this case, one variable would be the name of the family member and the another variable would be the date they were born. Django will automatically create a SQL table for this. More information about models can be found [here](https://docs.djangoproject.com/en/2.2/topics/db/models/).

- **Migration**: This is Django’s way of storing changes you make to your models (adding a field, deleting a model, etc.) into your database schema. More information about migrations can be found [here](https://docs.djangoproject.com/en/2.2/topics/migrations/).

- **Template**: Django needs a convenient way to generate HTML dynamically. A template contains the static parts of the desired HTML output as well as some special syntax describing how dynamic content will be inserted. 

## Commands
`python3 manage.py runserver`   
Starts development server on the internal IP at port 8000.

`python3 manage.py runserver 8080`   
A different port can be specified by adding it at the end of the argument. This example sets the port to 8080.

`python3 manage.py makemigrations`      
Tells Django that you’ve made some changes to your models and that you’d like the changes to be stored as a migration. 

`python3 manage.py migrate`     
Runs the migrations for you and manage your database schema automatically. This command takes all the migrations that haven’t been applied and runs them against your database - essentially, synchronizing the changes you made to your models with the schema in the database.

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
        templates/
            index.html
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

- **templates/**: Django will look for templates in here.