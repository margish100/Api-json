# Api-json

 heroku login
Enter your Heroku credentials.
Email: margishp100@gmail.com
Password (typing will be hidden):
Authentication successful.


Add a Procfile in the project root;
Add requirements.txt file with all the requirements in the project root;
Add Gunicorn to requirements.txt;
A runtime.txt to specify the correct Python version in the project root;
Configure whitenoise to serve static files.

Create a file named Procfile in the project root with the following content:

web: gunicorn bootcamp.wsgi --log-file -


If you are using a virtualenv and pip you can simply run:

pip freeze > requirements.txt


Django==1.9.8
dj-database-url==0.3.0
dj-static==0.0.6
gunicorn==19.6.0
Unipath==1.0
python-decouple==3
Pillow==3.3.0
Markdown==2.6.6
bleach==1.4.3
psycopg2==2.6.1
whitenoise==3.2

heroku addons:create heroku-postgresql:hobby-dev

heroku run python manage.py migrate
