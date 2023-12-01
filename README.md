PROJECT:

to use models.ImageField - <span style="color:red">pip install pillow

<span style="color:red">python manage.py migrate</span> ну надо после makemigrations 

to use models (команда, которой формируется база данных с которой будет работать приложение) - <span style="color:red">python manage.py makemigrations</span>

run server on localhost - <span style="color:red">python manage.py runserver

run server on LAN - <span style="color:red">python manage.py runserver 0.0.0.0:8000</span>

SUPERUSER:

to create - <span style="color:red">python manage.py createsuperuser

to change password - <span style="color:red">python manage.py changepassword admin </span> # (nickname)

superuser: {'login': <span style="color:red">'admin'</span>, 'password': <span style="color:red">'Vfkzdf2845'</span>}

MEDIA:

зачем-то надо в settings.py дописать это:

MEDIA_ROOT = os.path.join(BASE_DIR, 'media') 

тогда изменяется путь к медиа с <имя приложения>/media/images на /media/images/<имя приложения> 

Не забудь добавить резюме на главную страничку:
<a href="{% static 'portfolio/resume.pdf %}">Resume</a>
<br>

<p>{{ post.description|safe|truncatechars:100 }}</p>
truncatechars:100 - для отображения части текста (в символах)
safe - для включения обработки синтаксиса HTTP striptags - для сокрытия (вроде!)
