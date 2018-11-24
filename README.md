# DjangoBackendTutorial
This is a basic introduction to the Django Rest Framework.  I've posted this here so I can easily refer to it accross machines.

## Setup our Backend 

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

## Enter items into Database
Open the shell 
```
python manage.py shell
```
Enter actors into our SQLite database 
```
from actors.models import Actor
actor1 = Actor(
first_name="Tom",
last_name="Cruise",
dp="https://ia.media-imdb.com/images/M/MV5BMTk1MjM3NTU5M15BMl5BanBnXkFtZTcwMTMyMjAyMg@@._V1_UY317_CR14,0,214,317_AL_.jpg",
age=55
)
actor1.save()
actor2 = Actor(
first_name="Hugh",
last_name="Jackman",
dp="https://images-na.ssl-images-amazon.com/images/M/MV5BNDExMzIzNjk3Nl5BMl5BanBnXkFtZTcwOTE4NDU5OA@@._V1_UX214_CR0,0,214,317_AL_.jpg",
age=49
)
actor2.save()
```
Verify the entries
```
Actor.objects.all()
```
This should give the following output:
#### <QuerySet [<Actor: Actor object (1)>, <Actor: Actor object (2)>]>





So apparently to server is running one is localhost:8000(clientside react) and second is localhost:8080(django-api) So to see live application open http://localhost:8000 in your browser window
