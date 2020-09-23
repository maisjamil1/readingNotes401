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

- create users/`forms.py`


- in forms.py write :
```python
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm
from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):
    class Meta:
        model = CustomUser
        fields = ('username', 'email')

class CustomUserChangeForm(UserChangeForm):
    class Meta:
        model = CustomUser
        fields = ('username', 'email')
```

go to users/`admin.py` ----> add :
```python
from django.contrib import admin

from django.contrib.auth import get_user_model
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ['email', 'username',]

admin.site.register(CustomUser, CustomUserAdmin)


```
in ubuntu ---->
- `python manage.py makemigrations users`
- `python manage.py migrate`
- `python manage.py createsuperuser`
- `python manage.py runserver`
______________________________________________
- go to `settings.py`----> `import os`
- go to `settings.py`---->`TEMPLATES`--->`'DIRS': [os.path.join(BASE_DIR, 'templates')],`
- go to `settings.py`----> 
```python
LOGIN_REDIRECT_URL = 'home'
LOGOUT_REDIRECT_URL = 'home'
```


