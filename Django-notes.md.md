## Django (A python web framework) important notes !!!

#### first confirm python3 and pip3 are installed in your pc. (in windows python and pip) 

###### first go to your desired folder where you want to install django project, here "desktop" is that folder

`cd desktop`

###### install virtual environment. if requirement already satisfied, means virtual environment already installed
			
`pip3 install virtualenv`  


`pip install virtualenv` (for windows user)

###### create a virtualenv dir. here "myenv" is the dir name. you can give yours.

`virtualenv -p python3 myenv`


`virtualenv myenv` (for windows user)
      
`python3 -m venv project_name` (mac Os user)

###### activate virtualenv, if (myenv) appeard in command line, it means virtual environment activate successfully

`source myenv/bin/activate` (linux and mac OS user)

`.\myenv\scripts\activate` (for windows user)

###### install django version 2.2.10

`pip3 install django==2.2.10`
				
`pip install django==2.2.10` (for windows user)

###### start a django project named "django-site". you can give yours

`django-admin startproject django-site`
###### Get list of command line help for Django
`django-admin help`
 
###### changing directory to django project 
`cd django-site`

###### manage.py command line utility

`python3 manage.py help`

###### start django server

`python3 manage.py runserver`

`python manage.py runserver` (for windows user)

###### open browser and go to `127.0.0.1:8000`

###### Creating a app in django 
`python3 manage.py startapp pages`

## MySQL Database Settings in Django

###### First install mysqlclient by :
`pip3 install mysqlclient`

###### Then add those lines in settings.py given below :

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'database_name',
        'USER': 'database_username',
        'PASSWORD': 'database_password',
        'HOST': '127.0.0.1',
        'PORT': '3306',
    }
}

```

###### Then migrate database 
`python3 manage.py migrate`

###### Run the Django development server on a custom host
`python manage.py runserver 127.0.0.1:8001 \--settings=mysite.settings`

