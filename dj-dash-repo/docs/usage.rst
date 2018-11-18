=====
Usage
=====

To use dj-dash in a project, add it to your `INSTALLED_APPS`:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'dashboard.apps.DashboardConfig',
        ...
    )

Add middleware in settings.py

'django.contrib.messages.context_processors.messages',


Add dj-dash's URL patterns:

.. code-block:: python

    from dashboard import urls as dashboard_urls


    urlpatterns = [
        ...
        path('analytics/', include(dashboard_urls)),
        ...
    ]
