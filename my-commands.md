# My Commands

Install Git on Linux Ubuntu
$ sudo apt-get update (optional)
$ sudo apt-get install git

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

Django- Start Project/App
*   python -c "import django; print(django.get_version())"
*   mkdir name
*   cd name 
*   sudo apt-get install python-virtualenv
*   virtualenv --python=python3.4 myvenv (or 2.7, myvenv is name you choose)
*   source myvenv/bin/activate (myvenv is name you chose)
*   pip install -r requirements.txt (if needed)
*   pip install django==1.7.3 (or other version)                       
*   django-admin startproject projectname
*   python manage.py migrate
*   python manage.py runserver port# (port# is optional)
*   control-c
*   python manage.py startapp appname
*   python manage.py makemigrations appname
*   python manage.py sqlmigrate appname 0001 (sql alternative)
*   python manage.py shell
*   >>>> exit()
*   To exit virtual environment type deactivate                                

    <br><p>Packages</p>
    <p>pip install Jinja2</p>
    <p>pip install fabric</p>
    <p>sudo apt-get install fabric</p>
    <p>pip install django-debug-toolbar</p>
    <p>pip install South</p>
    <p>pip install Celery</p>
    <p>pip install djangorestframework</p>
    <p>pip install markdown # Markdown support for the browsable API</p>
    <p>pip install django-filter # Filtering support</p>
    <p>pip install djangorestframework-gis</p>
    <p>pip install django-localflavor</p>
    <p>pip install django-haystack</p>
    <p>pip install Pillow</p>    

    <br><p>Heroku- Main Commands to Deploy</p>
    <br><p>Heroku- Main Commands to Update</p>
