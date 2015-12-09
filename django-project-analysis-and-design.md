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

Template Inheritance
*   Base, Index
*   Base: {% load staticfiles %}
*   Non-Base: {% extends "base.html" %}

Generic Views (pk, not id)
*   TemplateView.as_view vs. include() (Models)
*   DetailView file name = <app name>/<model name>_detail.html
*   ListView file name = <app name>/<model name>_list.html

Django Workflow
*   Settings/Modules, Middleware
*   Global URLs, URLconfs, Shortcuts, Requests, Responses (HttpResponse, Http404), Redirects
*   URLs (arguments: regex, view, kwargs (arbitrary keyword arguments), name), (django.core.urlresolvers)
*   name.urls -> ROOT_URLCONF -> urlpatterns -> include () -> regex
*   Regex does not search domain name, GET or Post parameters
*   After regex match, Django calls view function with a HttpRequest as object as first argument...
*   Decorators
*   Class Based-Views, Built-In Views
*   DIRS, Templates/Includes, Static Files... (TEMPLATES, APP_DIRS = True (default), DjangoTemplates backend, INSTALLED_APPS -> subdirectory "templates")
*   "That code loads the template called polls/index.html and passes it a context. The context is a dictionary
mapping template variable names to Python objects."
*   appname file -> templates file -> appname file... template name = appname/filename.html
*   "The render() function takes the request object as its first argument, a template name as its second argument and a
dictionary as its optional third argument. It returns an HttpResponse object of the given template rendered with
the given context."
*   get_list_or_404()/filter(), get_object_or_404()/get()
*   Template Tags and Filters (filter value of variable), Humanization
*   Variable: model.attribute = output value
*   . also for dictionary-key lookup, index lookup, function calls
*   QuerySet/Field Lookups/Lookup Expressions

Database Schema/API
*   Models (In Module) -> Class (subclass of models.Model) -> Class Variables (database fields, some with required arguments for database validation) 
*   Primary Keys (IDs) added automatically, Foreign Key (id appended to field name), many-to-one, many-to-many, one-to-one

Shell
*  Bypass manage.py = django.setup()
*  manage.py sets DJANGO_SETTINGS_MODULE env variable, which gives Django the Python import path to your mysite/settings.py file

DevOps
*   DB
*   Postgres
*   Migrations
*   Test
*   Cache, Sessions
*   API

Additional
*   Sites
*   Admin: admin.site.register(models.Model)
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
   


