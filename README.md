# django-docker

Clone or download django-docker project to on your computer.

Create the Django project by running the docker-compose run command as follows.

    docker-compose run web django-admin startproject composeexample .

In your project directory, edit the settings.py file. Replace DATABASE section with the following:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```
Run the docker-compose up command from the top level directory for your project.

    docker-compose.exe up -d 

Enter docker machine.

    docker exec -it <container-id> bash

Create database migration

    python manage.py migrate

Create Super User.

    python manage.py createsuperuser
