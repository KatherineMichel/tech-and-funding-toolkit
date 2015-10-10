# my-commands

    <p>GitHub- General</p>
    <p>git clone https://github.com/username/reponame.git</p>
    <p>git clone --branch=gh-pages https://github.com/username/reponame.git</p>
    <p>git clone git@github.com:username/reponame.git</p>
    <p>git pull origin gh-pages</p>
    <p>git add .</p>
    <p>git commit . (or git commit -m . to avoid leaving message, or git commit -m -u . to also update files not on the PATH)</p>
    <p>note screen: a, type note, then esc :wq enter to exit</p>
    <p>git push origin master</p>
    <p>git push origin gh-pages</p>
    <p>git push repo-url master/gh-pages</p>
    <p>git merge --abort (to undo a merge)</p>
    <p>cd ~</p>                                

    <br><p>Django- Start Project/App</p>
    <p>python -c "import django; print(django.get_version())"</p>
    <p>mkdir name</p>  
    <p>cd name</p> 
    <p>sudo apt-get install python-virtualenv</p>  
    <p>virtualenv --python=python3.4 myvenv (or 2.7, myvenv is name you choose)</p> 
    <p>source myvenv/bin/activate (myvenv is name you chose)</p>  
    <p>pip install -r requirements.txt (if needed)</p> 
    <p>pip install django==1.7.3 (or other version)</p>                                
    <p>django-admin startproject projectname</p>  
    <p>python manage.py migrate</p> 
    <p>python manage.py runserver port# (port# is optional)</p> 
    <p>control-c</p> 
    <p>python manage.py startapp appname</p> 
    <p>python manage.py makemigrations appname</p> 
    <p>python manage.py sqlmigrate appname 0001 (sql alternative)</p>
    <p>python manage.py shell</p>
    <p>>>> exit()</p>
    <p>To exit virtual environment type deactivate</p>                                 

    <br><p>Heroku- Main Commands to Deploy</p>
    <br><p>Heroku- Main Commands to Update</p>
