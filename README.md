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

------------------------------------------------------------------------------------------------------------------

## settings.py

- installed apps is the list of django modules that we get loaded at startup, they form the start apps registry

## Databse
- storage, which engine?, how django connects to DB, how trans behaves, how migrations apply

## AUTH_USER_MODEL
 - We cannot use Django's default user model in productiom because:
   1. username fields conflics with modern auth
   2. no email-based login
   3. limited extensibilty
   4. adding fields later can break migrations
- so we define ours early "accounts.User" for instance

## rest_framework
- controls the default behaviour of our API service ie:
   1. What auth every view uses
   2. how error are formatted 
   3. how data is paginated
   4. how throthling works
   
   ------------------------------------------------------------------------------------------------------------

## Postgress to SQL lite
   + sql lite cannot handle concurrent writes
   + sql lacks many production faetures we reral on 
   + migrating later causes migrations and datatypes conflicts
   + postgres gives reliabilty  from day one 

   -------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## .env
   1. security & cryptographic values
      + <pre>SECRET_KEY </pre>
      + JWT signing keys
      + Auth creds
      --------------------------------------------------------------------------------------------------------------------------------------------------------------------
   2. DB credes
      <pre>USER</pre>
      <pre>NAME</pre>
      <pre>DB_PASSWORD</pre>
      <pre>DB_HOST</pre>
      <pre>DB_PORT</pre>
     -------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    3. Env mode
       <pre>DEBUG</pre>
       <pre>ENVIRONMENT</pre>

       -------------------------------------------------------------------------------------------------------------------------------------------------------------

    4. Allowed hosts & CORS
       <pre>ALLOWED_HOSTS</pre>
       <pre>CORS_ALLOWED_ORIGINS</pre>

       ------------------------------------------------------------------------------------------------------------------------------------------------------------------

    5. Third-party API keys
       <pre>EMAIL_API_KEY</pre>
       <pre>SMS_API_KEY</pre>

       ------------------------------------------------------------------------------------------------------------------------------------------------------------------

