Django AngularJS
================

`AngularJS <https://angularjs.org/>`_ 1.3.15

Requirements
------------

`Django <https://www.djangoproject.com/>`_ 1.4 or later

Installation
------------

::

    $ pip install django-static-angular==1.3.15

Setup
-----

Just add ``'django.contrib.staticfiles'`` and ``'django_static_angular'`` to INSTALLED_APPS in
your settings.py::

    INSTALLED_APPS = (
        # ...

        'django.contrib.staticfiles',
        'django_static_angular',

        # ...
    )

Refer to Django `static files <https://docs.djangoproject.com/en/dev/howto/static-files/>`_
documentation to configure and deploy static files.


Usage
-----

You can refer to angular in your template with::

    {% load staticfiles %}
    {% static 'static_angular/js/angular.js' %}

Admin template customization::

    {% load staticfiles %}

    {% extends "admin/base_site.html" %}

    {% block extrahead %}
        <script type="text/javascript" src="{% static 'static_angular/js/angular.js' %}" />
    {% endblock %}

Static files::

    static_angular/js/angular.js - AngularJS - v1.3.15
    static_angular/js/angular.min.js - AngularJS (min) - v1.3.15
    static_angular/js/angular.min.map - AngularJS (map) - v1.3.15

