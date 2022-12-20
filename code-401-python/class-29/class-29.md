#  API Deployment

## SSH: Understanding Encryption, Ports and Connection

### SSH is: Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

### How Does SSH Work?

- **Windows, you will need to utilize an SSH client to open SSH connections.**

- **The most popular SSH client is PuTTY**

## Different Encryption Techniques

**three different encryption technologies used by SSH:**

- Symmetrical encryption

- Asymmetrical encryption

- Hashing

## Symmetric Encryption

## Managing Django Settings: Issues

### Different environments:

**Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.**

### Sensitive data.

**You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.**

### Django settings are a Python code. 

**This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.**

## Django Configurations: Different Approaches

### The basic idea of this method is to extend all environment-specific settings in the settings_local.py file, which is ignored by VCS. Here’s an example:

### Pros:

- Secrets not in VCS.

### Cons:

-settings_local.py is not in VCS, so you can lose some of your Django environment settings.

- The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.

- You need to have settings_local.example (in VCS) to share the default Django configurations for developers.

## 2- Separate settings file for each environment

**It allows you to keep all configurations in VCS and to share default settings between developers.**

### Pros:

- All environments are in VCS.

- It’s easy to share settings between developers.

### Cons:

-You need to find a way to handle secret passwords and tokens.
“Inheritance” of settings can be hard to trace and maintain.

## 3- Environment variables

**issue with sensitive data, you can use environment variables in Django.**

### Pros:

- Django config is separated from code.

- Environment parity – you have the same code for all environments.

- No inheritance in settings, and cleaner and more consistent code.

- There is a theoretical grounding for using Django environment variables – 12 Factors.

### Cons:

-You need to handle sharing default config between developers.

## 12 Factors

**12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.**

### collection consists of twelve parts:

1-Codebase

2-Dependencies

3-Config

4- Backing services

5- Build, release, run

6- Processes

7- Port binding

8- Concurrency

9- Disposability

10-Dev/prod parity

11- Logs

12- Admin processes

## django-environ

**Django env variables are the perfect place to store settings.**

### Technically it’s a merge of:

1- envparse

2- honcho

3- dj-database-url

4- dj-search-url

5- dj-config-url

6- django-cache-url

### Setting Structure

**Instead of splitting settings by environments, you can split them by the source: Django, third- party apps (Celery, DRF, etc.), and your custom settings.**

## Naming Conventions

**simple rules for our custom (project) settings:**

- Give meaningful names to your settings.

- Always use the prefix with the project name for your custom (project) settings.

- Write descriptions for your settings in comments.

### Best Practices :

- Keep settings in environment variables.

- Write default values for production configuration (excluding secret keys and tokens).

- Don’t hardcode sensitive settings, and don’t put them in VCS.

- Split settings into groups: Django, third-party, project.

- Follow naming conventions for custom (project) settings.

