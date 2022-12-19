# Configuring Django Settings

## Managing Django Settings: Issues 

- **Different environments** : Each environment can have its own specific settings, You need an approach that allows you to keep all these Django setting configurations.
- **Sensitive data** : we should keep the sensitive data on SECRET _KEY 
- **Sharing settings between team members** 
- **Django settings are a Python code**


## Setting Django Configurations: Different Approaches

### settings_local.py

- **settings.py file**

```
ALLOWED_HOSTS = ['example.com']
DEBUG = False
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'production_db',
        'USER': 'user',
        'PASSWORD': 'password',
        'HOST': 'db.example.com',
        'PORT': '5432',
        'OPTIONS': {
            'sslmode': 'require'
        }
    }
}

...

from .settings_local import *
```

- **settings_local.py file**

```


ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}
```

## Separate settings file for each environment



```
settings/
   ├── __init__.py
   ├── base.py
   ├── ci.py
   ├── local.py
   ├── staging.py
   ├── production.py
   └── qa.py
```


To specify for a project you run which Django configuration to use, you need to set an additional parameter:

`python manage.py runserver --settings=settings.local`

---

# What Is SSH: Understanding Encryption, Ports and Connection


## What Is SSH?
SSH, or Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.


## Why Is SSH Used?
Secure Shell (SSH for short) is a network communication protocol that makes it possible for two computers to communicate with one another. SSH also makes data transfers possible between two computers.

