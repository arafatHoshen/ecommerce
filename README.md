![photo](https://nongareshop.pythonanywhere.com/static/app/images/banner/s2.jpg)

# Django E-commerce

A brief description of what this padfe sfddasdit's for


## How to Deployment

1. Create an account on Pythonanywhere
2. Create a Repositorie on GitHub 
3. Push your project to GitHub
4. Test django webapp and create django requirements files

```bash
  python manage.py runserver
  python -m pip freeze > requirements.txt
```
5. git clone 

6. mkvirtualenv --python=/usr/bin/python3.9 venv 
7. pip install -r requirements.txt
8. Setting up your Web app and WSGI file


```bash
  /home/nongareshop/ecommerce
  /home/nongareshop/
  /home/nongareshop/.virtualenvs/env

           # Paths
         /static/	/home/nongareshop/ecommerce/static/

         /media/	/home/nongareshop/ecommerce/media_root/
```
9. WSGI
import os
import sys


path = os.path.expanduser('~/ecommerce')

if path not in sys.path:
    sys.path.insert(0, path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'ecproject.settings'

from django.core.wsgi import get_wsgi_application

from django.contrib.staticfiles.handlers import StaticFilesHandler
application = StaticFilesHandler(get_wsgi_application())
