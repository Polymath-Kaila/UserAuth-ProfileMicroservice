# AUTH & PROFILES

## Steps

### 1. Create project folder & activate virtual environment

```bash
python -m venv venv
Activate it:

bash
Copy code
source venv/bin/activate

2. Install Django & DRF
bash
Copy code
pip install django djangorestframework
Upgrade pip:

bash
Copy code
pip install --upgrade pip

3. Create the Django project
bash
Copy code
django-admin startproject auth_service
Core Project Files
File	Purpose
settings.py	Main configuration module
urls.py	API endpoints routing
asgi.py	Async gateway
wsgi.py	Production gateway
__init__.py	Marks directory as module

settings.py Notes
Installed Apps
Modules loaded at startup. They form the application registry.

Database
Defines:

Storage engine

DB connection

Transaction behavior

Migration handling

Custom User Model (AUTH_USER_MODEL)
Reasons not to use Django’s default user model in production:

Username field conflicts with modern authentication

No email-based login

Limited extensibility

Adding fields later may break migrations

Define your custom model early, e.g. "accounts.User".

rest_framework Settings
Controls API behavior:

Authentication

Error formatting

Pagination

Throttling

PostgreSQL vs SQLite
SQLite cannot handle concurrent writes

Lacks production-grade features

Migrating later causes datatype & migration conflicts

PostgreSQL is reliable from day one

.env Structure
1. Security & Cryptographic Values
SECRET_KEY

JWT signing keys

Auth credentials

2. Database Credentials
USER

NAME

DB_PASSWORD

DB_HOST

DB_PORT

3. Environment Mode
DEBUG

ENVIRONMENT

4. Allowed Hosts & CORS
ALLOWED_HOSTS

CORS_ALLOWED_ORIGINS

5. Third-Party API Keys
EMAIL_API_KEY

SMS_API_KEY