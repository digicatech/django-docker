
Önceki imajları sil
docker rm -f $(docker ps -a -q) 
docker rmi $(docker images web_web -a -q)



docker-compose run web django-admin startproject composeexample .

docker-compose.exe up --build

sonrasinda docker start stop ile kapatilip açilabilir.

Bu dokümandaki yönergeler izlendi
https://docs.docker.com/compose/django/


Deploy İçin
https://dev.to/joekreydt/deploy-django-in-a-docker-container--41n6



settings.py de


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}


docker exec -it 2afbc064c57a bash

python manage.py migrate

python manage.py createsuperuser