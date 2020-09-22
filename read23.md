
# Django Custom User Model
Django ships with a built-in User model for authentication, however the official Django documentation highly recommends using a custom user model for new projects. The reason is if you want to make any changes to the User model down the road--for example adding a date of birth field--using a custom user model from the beginning makes this quite easy. But if you do not, updating the default User model in an existing Django project is very, very challenging.

So always use a custom user model for all new Django projects. However the official documentation example is not actually what many Django experts recommend using. There is a far easier yet still powerful approach to starting off new Django projects with a custom user model 

The Django auth app:

Django automatically installs the auth app when a new project is created.
Look in the config/settings.py file under INSTALLED_APPS and you can see auth is one of several built-in apps Django has installed for us.
Login Page:

To make our login page! Django by default will look within a templates folder called registration for auth templates.
The login template is called login.html.
Create a new directory called registration and the requisite login.html file within it.
From the command line type Control-c to quit our local server and enter the following commands:
 (accounts) $ mkdir templates
 (accounts) $ mkdir templates/registration
 (accounts) $ touch templates/registration/login.html
Create users:

we haven't created any users yet. Let's do that by making a superuser account from the command line.
Quit the server with Control+c and then run the command python manage.py createsuperuser.
Answer the prompts and note that your password will not appear on the screen when typing for security reasons.
Create a homepage

We want a simple homepage that will display one message to logged out users and another to logged in users.
First quit the local server with Control+c and then create new base.html and home.html files.
Note that these are located within the templates folder but not within templates/registration/ where Django auth looks by default for user auth templates.

