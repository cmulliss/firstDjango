# firstDjango

##Learning Django, virtualenv and github
<img src="setuptocat.jpg" alt="Octocat image" />

#####Roughly did the following, after setting up virtualenv and django via pip on system and adjusting my .bashrc or .bash_profile. Will add the details for this later
1. first create a directory and cd to it
2. create virtual environment: virtualevn env
3. activate it:  source ./env/bin/activate
4. deactivate when wanted
5. install django pip install django
6. pip freeze > requirements.txt
7. create your django project:  django-admin.py startproject firstDjango
8. git init
9. follow instructions on github
10. best to work on new branch
11. to add to another computer, clone then create virtualenv, activate, install django 
12. add, commit, push etc


####Experimented with virtualenvwrapper too, but less easy to backup via git / github as stores virtual environments outside repository
#####Setting up a django project with git and virtualenvwrapper

1. Make a directory for the environment and your projects mkdir virtualEnvs
2. mkvirtualenv virtaulEnv
then cd to virtual environments
3. pip install virtualenvwrapper
4. pip install django
5. pip freeze > requirements.txt
6. create django project: django-admin.py startproject firstDjango
7. copy your env folder from the ~/.virtualenvs/ folder to a backup folder in your new folder above, the one that contains your project
8. git init (previously create repo on github with no files)
9. git remote add origin remote repository URL (Sets the new remote)
10. git remote -v (Verifies the new remote URL)
11. git push origin master (Pushes the changes in your local repository up to the remote repository you specified as the origin)

####Seems like upon further research and reflection, might be better not saving the virual environment in my project, but just the info needed to recreate it:
1. pip freeze > requirements.txt (OK, already doing that)
2. can be loaded with: pip install -r requirements.txt
3. RyanBrady showed how you can string the deploy statements in a single line:
virtualenv --no-site-packages --distribute .env && source .env/bin/activate && pip install
4. will continue to experiment as this would presumably work with the wrapper?

