# Django Custom User

## Overview

Django's built-in User model and authentication support is incredible. It's been a staple of Django for a long time.


## Custom User Model

Creating our initial custom user model requires four steps:

- update django_project/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

In `settings.py` we'll add the accounts app and use the `AUTH_USER_MODEL` config to tell Django to use our new custom user model in place of the built-in `User` model.
We'll call our custom user model `CustomUser`.
Within `INSTALLED_APPS` add `accounts` at the bottom. Then at the bottom of the entire file, add the `AUTH_USER_MODEL` config.
