# Django : Custom User Model

**Django ships with a built-in User model for authentication and if you'd like a basic tutorial on how to implement log in, log out, sign up and so on see the Django Login and Logout tutorial for more.**

## To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code

- install Django

-make a new Django project called django_project

- make a new app accounts

- start the local web server

**Note:Note that we did not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.**

## AbstractUser vs AbstractBaseUser

**In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work.**

### Custom User Model

**Creating our initial custom user model requires four steps:**

- update django_project/settings.py

- create a new CustomUser model

- create new UserCreation and UserChangeForm

- update the admin

>>
    INSTALLED_APPS = [
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",
    "accounts",  # new
 ]
 ...
 AUTH_USER_MODEL = "accounts.CustomUser"  # new

2- **Now update accounts/models.py with a new User model which we'll call CustomUser.**
>>
    # accounts/models.py
 from django.contrib.auth.models import AbstractUser
 from django.db import models

 class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username


3-  **Stop the local server with Control+c and create a new file in the accounts app called forms.py.**

>>
  $ touch accounts/forms.py

4- **We'll update it with the following code to largely subclass the existing forms.**

>> 
     accounts/forms.py
    from django import forms
    from django.contrib.auth.forms import UserCreationForm, UserChangeForm

 from .models import CustomUser

 class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")

 class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ("username", "email")

5- **Finally we update admin.py since the Admin is highly coupled to the default User model.**

>> 
 # accounts/admin.py
    from django.contrib import admin
    from django.contrib.auth.admin import UserAdmin

    from .forms import CustomUserCreationForm, CustomUserChangeForm
    from .models import CustomUser

    class CustomUserAdmin(UserAdmin):
        add_form = CustomUserCreationForm
        form = CustomUserChangeForm
        model = CustomUser
        list_display = ["email", "username",]

    admin.site.register(CustomUser, CustomUserAdmin)

6- **And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.**
>>
    (.venv) > python manage.py makemigrations accounts
    (.venv) > python manage.py migrate

### Superuser

1- It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out.
>> 
    (.venv) > python manage.py createsuperuser

2- Templates/Views/URLs

    **Our goal is a homepage with links to log in, log out, and sign up. Start by updating settings.py to use a project-level templates directory.**

>> 
    django_project/settings.py
    TEMPLATES = [
    {
        ...
        "DIRS": [BASE_DIR / "templates"],  # new
        ...
    },
    ]

-  **django_project/settings.py**
>>
    LOGIN_REDIRECT_URL = "home"
    LOGOUT_REDIRECT_URL = "home"

- **accounts/urls.py**
>>
    from django.urls import path

    from .views import SignUpView

    urlpatterns = [
        path("signup/", SignUpView.as_view(), name="signup"),
    ]

-  **accounts/views.py**
>>
    from django.urls import reverse_lazy
    from django.views.generic.edit import CreateView
    from .forms import CustomUserCreationForm
    class SignUpView(CreateView):
        form_class = CustomUserCreationForm
        success_url = reverse_lazy("login")
        template_name = "registration/signup.html"

