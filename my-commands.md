# My Commands

Terminal
*   gnome-terminal
*   gedit

Install Git on Linux Ubuntu
*   sudo apt-get update (optional)
*   sudo apt-get install git
*   [GitHub Help](https://help.github.com/articles/set-up-git/#platform-linux)

GitHub- General</p>
*   git clone https://github.com/username/reponame.git
*   git clone --branch=gh-pages https://github.com/username/reponame.git
*   git clone git@github.com:username/reponame.git
*   git pull origin gh-pages
*   git add .
*   git commit . (or git commit -m . to avoid leaving message, or git commit -m -u . to also update files not on the PATH)
*   note screen: a, type note, then esc :wq enter to exit
*   git push origin master
*   git push origin gh-pages
*   git push repo-url master/gh-pages
*   git merge --abort (to undo a merge)
*   cd ~                              

Python
*   sudo apt-get install python-pip
*   sudo pip install virtualenv
*   python -V

Django 
*    python -c "import django; print(django.get_version())

Django- Start Project/App
*   mkdir name
*   cd name 
*   sudo apt-get install python-virtualenv
*   virtualenv --python=python3.4 myvenv (or 2.7, myvenv is name you choose)
*   source myvenv/bin/activate (myvenv is name you chose)
*   pip install -r requirements.txt (if needed)
*   pip install django==1.9 (or other version)                       
*   django-admin startproject projectname
*   python manage.py migrate
*   python manage.py runserver port# (port# is optional)
*   control-c
*   python manage.py startapp appname (cd same directory as manage.py)

Migrate
*   python manage.py migrate
*   python manage.py makemigrations appname
*   python manage.py sqlmigrate appname 0001 (sql alternative)

Shell
*   python manage.py shell

Django Project Mapping
*   Add each appname to projectname/settings.py INSTALLED_APPS
*   Add app_name = 'appname' to appname/views.py
*   projectname/urls.py = domain; appname/urls.py = domain/appname/
*   Add appname urls to projectname/urls.py:     url(r'^appname/', include('appname.urls')),
*   Map appname/urls.py to appname/views.py
*   Map "name" 

Templates and static
*   appname/templates/appname/filename.html
*   appname/static/appname/styles.css

Python Exit
*   >>>> exit()
*   To exit virtual environment type deactivate                                

Packages</p>
*   pip install Jinja2
*   pip install fabric
*   sudo apt-get install fabric
*   pip install django-debug-toolbar
*   pip install South
*   pip install Celery
*   pip install djangorestframework
*   pip install markdown # Markdown support for the browsable API
*   pip install django-filter # Filtering support
*   pip install djangorestframework-gis
*   pip install django-localflavor
*   pip install django-haystack
*   pip install Pillow

*   Heroku- Main Commands to Deploy
*   Heroku- Main Commands to Update

Two deployment approaches
*   Django Girls Tutorial approach
*   Bootcamp approach

Good Resources
*   Website Launch Checklist for Web Designers: https://github.com/tutsplus/Website-Launch-Checklist-for-Web-Designers
*   Staged Deployment
*   Deployment via AWS/Digital Ocean
*   Memcached: http://memcached.org
*   Django Debug Toolbar: https://django-debug-toolbar.readthedocs.org
*   Django Rest Framework: http://www.django-rest-framework.org
*   Django Local Flavor: https://django-localflavor.readthedocs.org/en/latest
*   Django Internationalization and Localization
*   GeoDjango
*   PostGIS
*   Django CMS: https://www.django-cms.org/en
*   Social Auth
*   Python Imaging Library
*   Haystack
*   South
*   Scrapy: http://scrapy.org
