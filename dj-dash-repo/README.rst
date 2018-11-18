=============================
dj-dash
=============================

.. image:: https://badge.fury.io/py/dj-dash-repo.svg
    :target: https://badge.fury.io/py/dj-dash-repo

.. image:: https://travis-ci.org/rahul1809/dj-dash-repo.svg?branch=master
    :target: https://travis-ci.org/rahul1809/dj-dash-repo

.. image:: https://codecov.io/gh/rahul1809/dj-dash-repo/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/rahul1809/dj-dash-repo

This is package for django site analytics

Documentation
-------------

The full documentation is at https://dj-dash-repo.readthedocs.io.

Quickstart
----------

Install dj-dash::

    pip install dj_dash_repo-0.1.0-py2.py3-none-any.whl

Add it to your `INSTALLED_APPS`:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'dashboard.apps.DashboardConfig',
        ...
    )

Add dj-dash's URL patterns:

.. code-block:: python

    from dashboard import urls as dashboard_urls


    urlpatterns = [
        ...
         path('analytics/', include(dashboard_urls)),
        ...
    ]

Add new middleware 
------------------
...
'dashboard.middleware.middlewares.SimpleMiddleware',
...

Do Makemgirations and migrate to create database for dashboard package
----------------------------------------------------------------------

python manage.py makemigrations dashboard


python manage.py migrate

Features
--------

* How many hits were made to the website? You can check the website traffic with 3 options either last 24 hours, last 1 hour or 30 days page visits

* From which countries user belonged?

* What were the devices used by the user to access the website?
* What is the average time taken to load a webpage?
* What languages were supported by the client side?
* What Browsers were used to access the site?

Running Tests
-------------

Does the code actually work?

::

    source <YOURVIRTUALENV>/bin/activate
    (myenv) $ pip install tox
    (myenv) $ tox

Credits
-------

Tools used in rendering this package:

*  Cookiecutter_
*  `cookiecutter-djangopackage`_

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`cookiecutter-djangopackage`: https://github.com/pydanny/cookiecutter-djangopackage
