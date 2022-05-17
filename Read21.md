# Django Best Practices: Custom User Model
`always use a custom user model for all new Django projects`

## how to implement one?

### Setup

To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called django_project
- make a new app accounts
- start the local web server

code

    (.venv) > python -m pip install django~=4.0.0
    (.venv) > django-admin startproject django_project .
    (.venv) > python manage.py startapp accounts
    (.venv) > python manage.py runserver

Note that we did not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.

### AbstractUser vs AbstractBaseUser

There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work

### Custom User Model

Creating our initial custom user model requires four steps:

- update django_project/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

In settings.py we'll add the name of app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model. We'll call our custom user model CustomUser.

Within INSTALLED_APPS add accounts at the bottom. Then at the bottom of the entire file, add the AUTH_USER_MODEL config.

    AUTH_USER_MODEL = "accounts.CustomUser" 

Now update accounts/models.py with a new User model which we'll call CustomUser.

We need new versions of two form methods that receive heavy use working with users. Stop the local server with Control+c and create a new file in the accounts app called forms.py.

We'll update it with the following code to largely subclass the existing forms.

Finally we update admin.py since the Admin is highly coupled to the default User model.

And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.

Superuser

It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.

#### Conclusion

Now that our custom user model is configured you can easily and at any time add additional fields to it.

You can also check out DjangoX, which is an open-source Django starter framework that includes a custom user model, email/password by default instead of username/email/password, social authentication, and more.

And if you'd like an even more in-depth example of starting a new Django project check out the book 