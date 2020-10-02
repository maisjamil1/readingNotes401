docker-compose up
poetry shell
poetry install
poetry add djangorestframework_simplejwt
poetry export -f requirements.txt -o requirements.txt
go to settings.py add:
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ],
    'DEFAULT_AUTHENTICATION_CLASSES':[
        'rest_framework_simplejwt.authentication.JWTAuthentication',
        'rest_framework.authentication.SessionAuthentication',
        'rest_framework.authentication.BasicAuthentication',
    ]
}
go to movies_project/urls.pyadd :
from rest_framework_simplejwt import views as jwt_views
#in urlpatterns add:
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
in settings add:
import os
STATIC_DIR = os.path.join(BASE_DIR, 'static')
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
STATIC_URL = '/static/'
STATICFILES_DIRS = [STATIC_DIR,]
docker-compose up --build
pip install httpie










poetry add djangorestframework_simplejwt
brew install httpie
 http 127.0.0.1:8000/api/v1/your app name/
http 127.0.0.1:8000/api/token/ username='your username' password='your password'
http 127.0.0.1:8000/api/v1/plants/ "Authorization: Bearer your token key"
poetry add gunicorn
docker-compose up --build
poetry add whitenoise
poetry export -f requirements.txt -o requirements.txt
docker-compose up --buil
