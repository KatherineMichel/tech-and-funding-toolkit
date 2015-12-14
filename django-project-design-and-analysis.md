Django Project Analysis and Design
===============

## Common Views/Functionality

Guidance
*   [Zed Shaw: Exercise 43: Basic Object-Oriented Analysis and Design](http://learnpythonthehardway.org/book/ex43.html)

*   Project vs. App
*   DRY Principle
*   Requirements
*   Site Map

*   [Example Website Sitemaps](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8)
*   [Google Search: Website Functionality Checklists](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8#q=website+functionality+checklist)
*   [Google Search: Website Functional Specification](https://www.google.com/search?q=example+website+sitemaps&rlz=1CAACAG_enUS625US635&oq=example+website+sitemaps&aqs=chrome..69i57j0j69i65l3j0.3579j0j7&sourceid=chrome&es_sm=0&ie=UTF-8#q=example+website+functional+specification)

Example Pages
*   Blog homepage
*   Entry “detail” page
*   Comment action
*   “index” page
*   “detail” page
*   "results” page
*   action

## Django

Overview
*   Settings
*   Middleware

Site Mappings
*   Modules, Classes
*   Models, Instances
*   Project URLs -> App URLs
*   Views
*   Templates/Includes (HTML), Template Inheritance
*   QuerySet/Field Lookups/Lookup Expressions/Context

Model Types
*   Many-to-many relationships
*   Many-to-one relationships
*   One-to-one relationships
 
Arguments
*  *args
*  **kwargs

Template Components
*   Variable = {{ variable }}
*   Tag = {% tag %} 
*   Filters = {{ variable|filter:"argument" }}
*   Comments = {% comment %}

Base Views
*   View
*   TemplateView
*   RedirectView

Generic Display Views
*   DetailView
*   ListView

Generic Editing Views
*   FormView
*   CreateView
*   UpdateView
*   DeleteView

Generic Date Views
*   ArchiveIndexView
*   TodayArchiveView
*   DateDetailView
*   DayArchiveView
*   WeekArchiveView
*   MonthArchiveView
*   YearArchiveView

Style
*   Static Files (CSS, JS, Images)

DevOps
*   DB
*   Postgres
*   Migrations
*   Test
*   API
*   Clickjacking Protection, Cross Site Request Forgery Protection, Cryptographic Signing
*   Cache, Sessions

User
*   Auth
*   Forms, Fields, Widgets

Place
*   Timezone, TZInfo, Internationalization, Localization, Translation
*   Geo

Properties and CMS
*   Admin
*   Sites
*   Content Types
*   Flatpages
*   Sitemap

Uploading, Downloading
*   Files
*   CSV/PDF

RSSy
*   Feed Generator, Syndication

Additional- Common
*   Decorators
*   Email
*   Paginator
*   Humanization

Additional- Less Common
*   Encoding
*   Six
*   Mixins
*   Jython
