
# Django Custom User Model
Django ships with a built-in User model for authentication, however the official Django documentation highly recommends using a custom user model for new projects. The reason is if you want to make any changes to the User model down the road--for example adding a date of birth field--using a custom user model from the beginning makes this quite easy. But if you do not, updating the default User model in an existing Django project is very, very challenging.

So always use a custom user model for all new Django projects. However the official documentation example is not actually what many Django experts recommend using. There is a far easier yet still powerful approach to starting off new Django projects with a custom user model 

