# DjangoBackendTutorial
This is a basic introduction to the Django Rest Framework.  I've posted this here so I can easily refer to it accross machines. Note that I am running this on Linux Ubuntu 18.04 LTS.  Note that I did not create this tutorial, I am have simply gone through it and found it to be a particularly useful beginner guide and posted here for convenience sake.  The original tutorial can be found at [Django for React/Angular/Mobile Apps](https://hackernoon.com/django-for-react-angular-mobile-apps-part-1-9d2804555ea8)

#### Following the steps below, you should be able to reproduce the below screenshot:
![django](https://user-images.githubusercontent.com/8731829/48966253-a2becb80-ef82-11e8-949f-f10efadd1b8d.png)


## Setup Backend 

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


## Enter Objects Into Database
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

## Run Server

Start server for your REST-API:-
```
./manage.py runserver
```


## View in Browser

enter http://localhost:8000 in your browser window
