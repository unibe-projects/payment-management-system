# aplicaciones

# Instalar Django

- instalar desde este paquete: https://www.python.org/downloads/release/python-3122/

- ademas configurar las variabñes de entorno en windows asi:

- C:\Users\PC\AppData\Local\Programs\Python\Python312\Scripts\
- C:\Users\PC\AppData\Local\Programs\Python\Python312\

- python --version
- pip --version
- pip install --upgrade pip
- pip install virtualenv
- virtualenv webapp
- cd webapp
- pip install Django
- - cd el viratual y activar el vitualizador
- python 
- import django
- django.get_version()
- exit()
- django-admin startproject webapp
- cd webapp
- python.exe manage.py migrate
- python.exe manage.py runserver
- python.exe manage.py startapp blog
- python.exe manage.py makemigrations blog
- python.exe manage.py blog sqlmigrate 0001
- python.exe manage.py migrate
- python.exe manage.py createsuperuser
- python.exe manage.py shell
- from django.contrib.auth.models import User
- from blog.models import Post
- us =User.objects.get(username='steveen')
- post = Post(title ='titulo',slug='afuera',body='es un post',author=us)
- post.save()

# actualiza

## Obtener el objeto Post que quieres actualizar
post = Post.objects.get(title='titulo')

## Actualizar los campos necesarios
post.title = 'Nuevo título'
post.body = 'Nuevo cuerpo del post'

# Guardar los cambios
post.save()

# Eliminar

## Obtener el objeto Post que quieres eliminar
post = Post.objects.get(title='titulo')

## Eliminar el objeto
post.delete()

