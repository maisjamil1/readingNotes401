- `rm -rf nnnnn`

- `mkdir django-custom-user`
- `cd django-custom-user`
- `mkdir CustomUser`
- `cd CustomUser`
- `poetry init -n`
- `poetry add django`
- `poetry add --dev black`
- `poetry shell`
- `django-admin startproject custom_user_project .`
- `python manage.py startapp users`
-  `python manage.py runserver`&#x1F534;: DO NOT DO python manage.py migrate
_____________________________________________________________
go to `settings.py` ----> 
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'users.apps.UsersConfig', #or 'users'
]
AUTH_USER_MODEL = 'users.CustomUser'

```
go to `users/models.py` ----> 
```python
from django.db import models
from django.contrib.auth.models import AbstractUser
class CustomUser(AbstractUser):
    pass

    def __str__(self):
        return self.username
```


