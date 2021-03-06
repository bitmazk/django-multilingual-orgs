Django Multilingual Orgs
========================

An app for showing localized versions of organization profiles. E.g. as plugin
in a blog post.

Comes with a django-cms plugin and is multilingual.

Prerequisites
-------------

You will need to have the following packages installed:

* django-cms (cms 3 beta ready)


Installation
------------

If you want to install the latest stable release from PyPi::

    $ pip install django-multilingual-orgs

If you feel adventurous and want to install the latest commit from GitHub::

    $ pip install -e git://github.com/bitmazk/django-multilingual-orgs.git#egg=multilingual_orgs

Add ``multilingual_orgs`` to your ``INSTALLED_APPS``::

    INSTALLED_APPS = (
        ...,
        'multilingual_orgs',
    )

Run the South migrations::

    ./manage.py migrate multilingual_orgs


Usage
-----

Use the Django admin to create your organization objects. If you are using
django-cms you can use the ``Organization Plugin`` to display an organization
in your placeholders.


Settings
--------

ORGANIZATION_PLUGIN_DISPLAY_TYPE_CHOICES
++++++++++++++++++++++++++++++++++

Default::

    [
        ('small', _('small')),
        ('big', _('big')),
    ]

When using the ``Organization Plugin`` in your django-cms placeholders you will
notice that you only have two choices for the ``Display type``. This field
can be helpful when you want to render an organization differently in different
parts of your site. If you need even more display types, just set this setting
to a different list of tuples.


Roadmap
-------

Check the issue tracker on github for milestones and features to come.
