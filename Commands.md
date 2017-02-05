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

## git command to clone: <a name="git-command-to-clone"></a>
```bash
$ git clone https://<USER>:<PASS>@github.com/<OWNER>/<REPO_NAME>.git <workspace>
```
##### where you replace-  
* <USER> with your GitHub username;
* <PASS> with your GitHub password;
* <OWNER> with the username of the person who owns the repository;
* <REPO_NAME> with the name of your project’s repository; and
* <workspace> with the name for your workspace directory. This is optional; leaving this option
out will simply create a directory with the same name as the repository.        

##### To tell Git your full name, and your e-mail address:
```bash
$ git config user.name "John Doe"
$ git config user.email "johndoe123@me.com"
````    