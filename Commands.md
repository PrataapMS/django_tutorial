# Quick Reference Commands

## Index:
- [Git Command to Clone](#git-command-to-clone)

## Install virtualenv via pip:  
```bash
$ sudo pip install virtualenv
```

## Create a virtual environment for a project:  
```bash 
$ cd my_project_folder
$ virtualenv venv
```

## To activate the virtual environment: 
```bash 
$ source venv/bin/activate
```

## Install required django version using pip:   
```bash
pip install Django==1.10.5
```

## Install packages as usual, for example:
```bash 
$ pip install requests
```

## To deactivate the virtual environment:   
```bash 
$ deactivate
```

## Check Django version:
```bash
python -m django --version
```

## To start new django project:
```bash 
django-admin startproject mysite
```

## To start the server: 
```bash
python manage.py runserver
```

##### To tell Git your full name, and your e-mail address:
```bash
$ git config user.name "John Doe"
$ git config user.email "johndoe123@me.com"
````    

## git command to clone:
```bash
$ git clone https://<USER>:<PASS>@github.com/<OWNER>/<REPO_NAME>.git <workspace>
            --------OR-------
$ git clone https://<Repo_name>.git
```
##### where you replace-  
* <USER> with your GitHub username;
* <PASS> with your GitHub password;
* <OWNER> with the username of the person who owns the repository;
* <REPO_NAME> with the name of your project’s repository; and
* <workspace> with the name for your workspace directory. This is optional; leaving this option
out will simply create a directory with the same name as the repository.        


## Create/add a new app to django
```bash
python manage.py startapp rango
```

## Creating and Migrating the Database
```bash
$ python manage.py migrate

# create a superuser to manage the database
$ python manage.py createsuperuser
```

## Creating / Updating Models / Tables
```bash
$ python manage.py makemigrations rango

# apply these migrations (which will essentially create the database tables), then you need to issue
$ python manage.py migrate
```

:warning: **Warning:**
> Whenever you add to existing models, 
> you will have to repeat this process running python manage.py makemigrations <app_name>, 
> and then python manage.py migrate


## Django shell
```bash
$ python manage.py shell
```

## Command to check query generated while performing query from django dbshell
*below represents an example which prints the sql query generated for a query perfrmed from django model interface
```bash
from django.db import connection
from django.db import reset_queries
reset_queries()
q = EoDTimeSeries.objects.filter(profile__NSEcode="ABB")
print (q.query)
```