# my-bash-workflow-cheatsheet
Cheat sheet for my bash/zsh workflow right now.

## Git
```git config user.name "${name}"``` - Set the user name locally. (In .git/config).
```git config user.email ${email}``` - Set the user email locally. (In .git/config).

## Bash

```chgrp -R ${groupName} ${directory}``` - Change the group ownership of all files and folders recursively in a root folder and for the root folder itself.  
```ls -a ${directoryName}``` - View contents of a folder along with the hidden files.  
```ls -altr ${directoryName}``` - View contents of a folder in detail.  
```ls -ld ${directoryName}``` - Check the permissions of a directory instead of contents.  
```ssh-keygen -t ed25519 -C "${email}"``` - Generate ssh keys for an email.  

## Docker

```docker-compose -f dev.yml up ${imageName}``` -  Run an image with imageName in docker.  
```test -z "$(docker ps -q 2>/dev/null)" && osascript -e 'quit app "Docker"'``` - Stop docker for mac gracefully. It requires that all the containers are in the stopped state.  
```docker ps -q | xargs -L1 docker stop``` - Stop all Docker containers without confirmation (dangerous if running something).  
```open --background -a Docker``` - Start Docker gracefully. It may take up to a minute for Docker to fully start.  

## Python
### Core
```python -m ${libraryName} --version``` - Check if and what version of a python library is installed.  
```python -m pip install ${libraryName}``` - Install a library with pip. It can also be run as pip install ${libraryName}.  
### Django
```django-admin startproject helloworld``` - Set up a new project for Django.  
```python manage.py runserver``` - Run Django webserver.  
```python manage.py runserver ${ip}:${port}``` - If you want to change the server’s IP, pass it along with the port. For example, to listen on all available public IPs (which is useful if you are running Vagrant or want to show off your work on other computers on the network.)  
```python manage.py makemigrations ${app}``` - By running makemigrations, you’re telling Django that you’ve made some changes to your models (in this case, you’ve made new ones) and that you’d like the changes to be stored as a migration.  
```python manage.py sqlmigrate ${app} ${version}``` - Convert migration file into a proper SQL query.  
### Jupyter Notebook
```jupyter-lab``` - Launch Jupyter Lab in the browser.