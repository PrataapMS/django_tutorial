## Footnotes

1. This assumes that you are using the IP address 127.0.0.1 and port 8000 when running your Django development web server. If you do not explicitly provide a port to run the development server on, Django defaults to port 8000 for you.
2. There are many applications available out there that you can use in your project. Take a look at PyPI and Django Packages to search for reusable apps which you can drop into your projects.


## Adding a Model
The workflow for adding models can be broken down into five steps.

First, create your new model(s) in your Django application’s models.py file.
Update admin.py to include and register your new model(s).
Then perform the migration $ python manage.py makemigrations
Apply the changes $ python manage.py migrate. This will create the necessary infrastructure within the database for your new model(s).
Create/Edit your population script for your new model(s).