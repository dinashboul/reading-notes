# Django introduction

## Django is a high-level Python web framework that enables rapid development of secure and maintainable websites. Built by experienced developers, Django takes care of much of the hassle of web development.

### Complete:

**Django follows the "Batteries included" philosophy and provides almost everything developers might want to do "out of the box".**


### Versatile

**Django can be (and has been) used to build almost any type of website — from content management systems and wikis, through to social networks and news sites.**

### Secure

**Django helps developers avoid many common security mistakes by providing a framework that has been engineered to "do the right things" to protect the website automatically.** 

### Scalable

**Django uses a component-based "shared-nothing" architecture (each part of the architecture is independent of the others, and can hence be replaced or changed if needed).**

### Maintainable

**Django code is written using design principles and patterns that encourage the creation of maintainable and reusable code. In particular, it makes use of the Don't Repeat Yourself (DRY) principle so there is no unnecessary duplication, reducing the amount of code.**

### Portable

**Django is written in Python, which runs on many platforms.** 

### Is Django opinionated?
**Web frameworks often refer to themselves as "opinionated" or "unopinionated".**

### What does Django code look like?

![image](./basic-django.png)

- URLs

- View

- Models
- Templates

### Sending the request to the right view (urls.py)

**A URL mapper is typically stored in a file named urls.py.**

### Handling the request (views.py)

**Views are the heart of the web application, receiving HTTP requests from web clients and returning HTTP responses. In between, they marshal the other resources of the framework to access databases, render templates, etc.**

### Rendering data (HTML templates)

**Template systems allow you to specify the structure of an output document, using placeholders for data that will be filled in when a page is generated. Templates are often used to create HTML, but can also create other types of document.**

### Defining data models (models.py)

**Django web applications manage and query data through Python objects referred to as models.**

### Django include

- Forms
- User authentication and permissions: Django includes a robust user authentication and permission system that has been built with security in mind.

- Caching

- Administration site
- Serializing data
