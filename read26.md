- `mkdir drf-api`
- `cd drf-api`
- `poetry init -n`
- `poetry add django djangorestframework`
- `poetry shell`
- `django-admin startproject movies_project .`
- `python manage.py  migrate`
- `python manage.py  startapp movie`
- `python manage.py  createsuperuser`
- `python manage.py  runserver`
______________________________________________
- in the `settings.py` ---> INSTALLED_APPS --->add the app to project applications `'movie.apps.MovieConfig',`
- go to `movie/models.py` ----> 
```python
from django.contrib.auth import get_user_model
from django.db import models

class Movies(models.Model):
    author = models.ForeignKey(get_user_model(), on_delete=models.CASCADE)
    title = models.CharField(max_length=64)
    body = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

    def __str__(self):
        return self.title

```
- `python manage.py makemigrations movie`
- `python manage.py migrate`

- go to  movie/`admin.py` ----> add :
```python
from django.contrib import admin

from .models import Movies
# Register your models here.

admin.site.register(Movies)

```
- `python manage.py runserver`
- do tests


