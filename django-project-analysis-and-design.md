# Django Project Analysis and Design

## Common Views/Functionality

Guidance
*   [Zed Shaw: Exercise 43: Basic Object-Oriented Analysis and Design](http://learnpythonthehardway.org/book/ex43.html)
*   [Example Website Sitemaps](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8)
*   [Google Search: Website Functionality Checklists](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8#q=website+functionality+checklist)
*   [Google Search: Website Functional Specification](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8#q=example+website+functional+specification)

Page Examples
*   Blog homepage
*   Entry “detail” page
*   Year-based archive page
*   Month-based archive page
*   Day-based archive page
*   Comment action

*   “index” page
*   “detail” page
*   "results” page
*   action

## Requirements
*   [Product Requirements Document Wikipedia](http://en.wikipedia.org/wiki/Product_requirements_document)
*   [Requirement Wikipedia](https://en.wikipedia.org/wiki/Requirement)
*   [Functional Requirement Wikipedia](https://en.wikipedia.org/wiki/Functional_requirement)
*   [Non-Functional Requirement Wikipedia](https://en.wikipedia.org/wiki/Non-functional_requirement)
*   [Specification Wikipedia](https://en.wikipedia.org/wiki/Specification_(technical_standard))
*   [Functional Specification Wikipedia](https://en.wikipedia.org/wiki/Functional_specification)
*   [Requirement Analysis Wikipedia](https://en.wikipedia.org/wiki/Requirements_analysis)
*   [Requirement Prioritization Wikipedia](https://en.wikipedia.org/wiki/Requirement_prioritization)
*   [Requirement Management Wikipedia](http://en.wikipedia.org/wiki/Requirements_management)

## Django

Django Workflow
*   Settings/Modules, Middleware
*   Global URLs
*   URLs
*   Decorators
*   Views, Generic Views
*   Templates/Includes, Template Inheritance, Static Files
*   Template Tags and Filters, Humanization
*   QuerySet/Field Lookups/Lookup Expressions

DevOps
*   DB
*   Postgres
*   Migrations
*   Test
*   Cache, Sessions
*   API

Additional
*   Sites
*   Admin
*   Auth
*   Timezone, TZInfo, Internationalization, Localization, Translation
*   Flatpages, Sitemap
*   Forms, Fields, Widgets
*   Email
*   Files
*   Paginator
*   Feed Generator, Syndication
*   Content Types
*   CSV/PDF
*   Geo
*   Encoding
*   ContentTypes
*   Six
*   Mixins
*   Clickjacking Protection, Cross Site Request Forgery Protection, Cryptographic Signing
*   Jython
   
Notes

Project vs. App
DRY Principle

Object-Oriented Programming
*   Class
*   Object, Object-Relational Mapper
*   Instances, Related Objects

Default INSTALLED_APPS 
*   django.contrib.admin 
*   django.contrib.auth
*   django.contrib.contenttypes
*   django.contrib.sessions
*   django.contrib.messages
*   django.contrib.staticfiles 

Revisit: Testing, Admin, Reusable Apps, Deployment Checklist, Writing Your First Path
Reference: model field reference

Database Schema/API
*   Models (In Module) -> Class (subclass of models.Model) -> Class Variables (database fields, some with required arguments for database validation) 
*   Primary Keys (IDs) added automatically, Foreign Key (id appended to field name), many-to-one, many-to-many, one-to-one

Template Inheritance
*   Base, Index
*   Base (or Index): {% load staticfiles %}, <link rel="stylesheet" type="text/css" href="{% static 'appname/style.css' %}" />
*   Non-Base: {% extends "base.html" %}
*   app_name = 'appname', {% url 'templatename' %} or {% url 'appname:templatename' %}
*   add app name to INSTALLED_APPS, run manage.py migrate, manage.py makemigrations

Generic Views (pk, not id)
*   from django.views import generic
*   TemplateView.as_view vs. include() (Models)
*   IndexView
*   DetailView file name = <app name>/<model name>_detail.html (question_id becomes pk)
*   ResultsView (DetailView)
*   ListView file name = <app name>/<model name>_list.html

*   Admin: admin.site.register(models.Model)

*   DIRS, TEMPLATES, APP_DIRS = True (default), DjangoTemplates backend, INSTALLED_APPS -> subdirectory "templates"
*   appname folder -> templates folder -> appname folder... template name = appname/filename.html (appname/templates/appname/filename.html)
*   STATICFILES_FINDERS, AppDirectoriesFinder -> INSTALLED_APPS -> subdirectory "static"
*   appname folder -> static folder -> appname folder... css file name = style.css (appname/static/appname/style.css)
*   appname/static/appname/images
*   name.urls -> ROOT_URLCONF -> urlpatterns -> include () -> regex
*   Regex does not search domain name, GET or Post parameters
*   After regex match, Django calls view function with a HttpRequest as object as first argument...

*   "That code loads the template called polls/index.html and passes it a context. The context is a dictionary
mapping template variable names to Python objects."
*   "The render() function takes the request object as its first argument, a template name as its second argument and a
dictionary as its optional third argument. It returns an HttpResponse object of the given template rendered with
the given context."
*   get_list_or_404()/filter(), get_object_or_404()/get()
*   for loop = method call
*   "request.POST is a dictionary-like object that lets you access submitted data by key name. In this case,
request.POST[’choice’] returns the ID of the selected choice, as a string. request.POST values are
always strings. Note that Django also provides request.GET for accessing GET data in the same way"
*   "After incrementing the choice count, the code returns an HttpResponseRedirect rather than a normal
HttpResponse. HttpResponseRedirect takes a single argument: the URL to which the user will be
redirected. We are using the reverse() function... "
*   request is an HttpRequest object
*   Variable: model.attribute = output value
*   . also for dictionary-key lookup, index lookup, function calls
*   Class Based-Views, Built-In Views
*   URLs (arguments: regex, view, kwargs (arbitrary keyword arguments), name), (django.core.urlresolvers)
*   URLconfs, Shortcuts, Requests, Responses (HttpResponse, Http404), Redirects
*   Filters (filter value of variable),
*   You can change STATIC_URL (used by the static template tag to generate its URLs
*   Admin: TabularInline, StackedInline
*   "By default, Django displays the str() of each object. But sometimes it’d be more helpful if we could display
individual fields. To do that, use the list_display admin option, which is a tuple of field names to display, as
columns, on the change list page for the object"
*   Admin list display = model fields, (list_display, list_filter, search_fields (will search str output using LIKE query)
*   class Name(models.Model): ... def methodname(self): return ... attributes 
*   Change list pagination, search boxes, filters, date-hierarchies, and column-header-ordering
*   "templates that belongs to a particular application, we should put in the application’s template
directory (e.g. polls/templates) rather than the project’s (templates)."
*   https://github.com/django/django/tree/master/django/contrib/admin/templates
*   Reusable app: djangoappname, djangoappname/README.rst, djangoappname/LICENSE file, djangoappname/setup.py, djangoappname/docs, djangoappname/MANIFEST.in 
*   "Each model is a Python class that subclasses django.db.models.Model.Each attribute of the model represents a database field." API/Queries
*   Reserved model field words: clean, save, delete
*   Model field class = column type, default widget, minimal validation requirements
*   Required argument example: CharField (and its subclasses) require a max_length argument
*   Common model arguments: null, blank, choices (list or tuple), default, help_text, primary_key (True), ect
*   "If you don’t specify primary_key=True for any fields in your model, Django will automatically add an
IntegerField to hold the primary key, so you don’t need to set primary_key=True on any of your
fields unless you want to override the default primary-key behavior. For more, see Automatic primary key fields. The primary key field is read-only. If you change the value of the primary key on an existing object and then
save it, a new object will be created alongside the old one."

Shell
*  Bypass manage.py = django.setup()
*  manage.py sets DJANGO_SETTINGS_MODULE env variable, which gives Django the Python import path to your mysite/settings.py file

*   context_object_name = overrides automatically generated context variable
*   Avoiding race conditions using F()

Add a DIRs option:
TEMPLATES = [
{
'BACKEND': 'django.template.backends.django.DjangoTemplates',
'DIRS': [os.path.join(BASE_DIR, 'templates')],
'APP_DIRS': True,
'OPTIONS': {
'context_processors': [
'django.template.context_processors.debug',
'django.template.context_processors.request',
'django.contrib.auth.context_processors.auth',
'django.contrib.messages.context_processors.messages',
],
},
}
]

Non-Base
{% extends 'base.html' %}
{% load staticfiles %}
{% load i18n %}

{% load humanize %}

{% block title %} Name {% endblock %}

{% block head %}
  <link href="{% static 'css/style.css' %}" rel="stylesheet">
{% endblock head %}

{% block main %}
{% endblock main %}

Scroll bar: page 91
