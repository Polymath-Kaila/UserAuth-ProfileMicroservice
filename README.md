# AUTH & PROFILES
## STEPS
1. create a folder, open in vs code then activate virtual envionment by running:
```bash
python -m venv venv
```
```bash

source venv/bin/activate

```

------------------------------------------------------------------------------------------------------------------
2. install django restframework
```bash 

pip install django djangorestframework

```
upgrade pip by running 

```bash
pip install --upgrade pip

```
------------------------------------------------------------------------------------------------------------------
3. Create the django project

```bash
django-admin startproject auth_service

```
------------------------------------------------------------------------------------------------------------------
## files

settings.py -->config brain
urls.py     -->API endpoints
asgi.py     -->async gateway
wsgi.py     -->production gateway
__init__.py -->makes it a module