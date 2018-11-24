# DjangoBackendTutorial


# Backend-Setup 

clone the repositroy:-
```
git clone https://github.com/vinitraj10/Django-React-Blog 
```
Create Virtualenv for django:-
```
virtualenv -p python3 mobileBackend && cd mobileBackend
```
Activate Virtual env:-
```
source bin/activate
```
Install Djangorestframework:-
```
pip install django djangorestframework
```
Make Migrations:-
```
./manage.py makemigrations
./manage.py migrate
```
Start server for your REST-API:-
```
./manage.py runserver
```

So apparently to server is running one is localhost:8000(clientside react) and second is localhost:8080(django-api) So to see live application open http://localhost:8000 in your browser window
