Django Documentation Contribution
As part of my contribution, I have created a well-structured and beginner-friendly guide covering essential topics in Django such as views, templates, and models. This documentation helps new developers by offering clear explanations, code examples, and references to Django's official documentation.

Table of Contents
Introduction
Views
Function-based Views
Class-based Views
Templates
Template Inheritance
Models
Defining Models
Additional Resources
Introduction
Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. This guide focuses on simplifying key concepts of Django and providing code examples that are easy to follow.

Views
Views in Django are responsible for handling web requests and returning the appropriate web responses. Think of views as the part of the code that decides what gets displayed when a user accesses a particular page or URL.

Function-based Views
Function-based views (FBVs) are one of the simplest ways to create views in Django. They are Python functions that return an HTTP response.

Example:
python code
# views.py

from django.http import HttpResponse

def hello_world(request):
    return HttpResponse("Hello, world!")
In the example above, hello_world is a function that returns a simple text response "Hello, world!" when accessed.

To make this function accessible through a URL, you need to add it to urls.py:

python code
# urls.py

from django.urls import path
from . import views

urlpatterns = [
    path('', views.hello_world),  # Maps the root URL ('/') to the hello_world view
]
For more details on Function-based Views, visit the official Django documentation.

Class-based Views
Class-based views (CBVs) allow for a more modular and reusable approach to writing views. This is particularly useful when you want to share functionality between views.

Example:
python code
# views.py

from django.http import HttpResponse
from django.views import View

class HelloWorldView(View):
    def get(self, request):
        return HttpResponse("Hello, world from Class-based View!")
In this example, a class named HelloWorldView handles the GET request and returns the response "Hello, world from Class-based View!".

To link this class-based view in your URLs, add it to urls.py:

python code
# urls.py

from django.urls import path
from .views import HelloWorldView

urlpatterns = [
    path('cbv/', HelloWorldView.as_view()),  # Maps /cbv/ to the HelloWorldView
]
For more on Class-based Views, refer to the official Django documentation.

Templates
Django templates allow you to define the structure and layout of HTML files separate from your Python code. This separation of concerns makes it easier to maintain both your front-end and back-end code.

Template Inheritance
Template inheritance allows you to reuse common elements (like headers or footers) across multiple pages. You define a base layout and then extend it to create individual page templates.

Example:
Base template: base.html

html

<!-- base.html -->
<!DOCTYPE html>
<html>
<head>
    <title>{% block title %}My Site{% endblock %}</title>
</head>
<body>
    <header>
        <h1>Welcome to My Site</h1>
    </header>
    
    <main>
        {% block content %}{% endblock %}
    </main>
    
    <footer>
        <p>© 2024 My Site</p>
    </footer>
</body>
</html>
Extending template: home.html

html code
<!-- home.html -->
{% extends "base.html" %}

{% block title %}Home{% endblock %}

{% block content %}
    <p>This is the home page content.</p>
{% endblock %}
In the above example, home.html extends base.html and only overrides the specific sections (title and content).

For more on Django Templates, check out the official documentation.

Models
Django models allow you to define the structure of your data in Python classes. These classes are then used to create, retrieve, update, and delete records in your database.

Defining Models
Here's an example of a model representing a Book entity:

python code
# models.py

from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)  # The title of the book
    author = models.CharField(max_length=100)  # Author's name
    published_date = models.DateField()  # Date when the book was published
    isbn = models.CharField(max_length=13)  # ISBN number of the book

    def __str__(self):
        return self.title  # String representation of the object
Once you’ve defined the model, apply it to the database by running:

 command
python manage.py makemigrations
python manage.py migrate
You can interact with the model using Django's ORM (Object-Relational Mapping) in the Python shell:

python code
# Shell commands

# Create a new book entry
book = Book.objects.create(title="Django for Beginners", author="William Vincent", published_date="2020-01-01", isbn="1234567890123")

# Retrieve all books
books = Book.objects.all()

# Retrieve a specific book
book = Book.objects.get(id=1)

# Update a book
book.title = "Advanced Django"
book.save()

# Delete a book
book.delete()
For further exploration of Django models, refer to the official documentation.

Additional Resources
Django Official Documentation
Django Views
Django Templates
Django Models