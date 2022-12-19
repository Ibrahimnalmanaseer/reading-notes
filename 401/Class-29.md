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

settings_local.py file:

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


