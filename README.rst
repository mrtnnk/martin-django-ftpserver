=================
Django FTP server
=================

|build-status| |pypi| |docs|

FTP server application that used user authentication of Django.

Getting Started
===============

1.  Install django-ftpserver by pip.

::

   $ pip install django-ftpserver

2. Add line to settings.INSTALLED_APPS for your django project.

::

   INSTALLED_APPS = (
       # ..
       'django_ftpserver',
   )

3. Migrate app.

::

   $ python manage.py migrate

4. Create FTP user group.

::

   $ python manage.py createftpusergroup my-ftp-group

5. Create FTP user account.

::

   $ python manage.py createftpuseraccount <username> my-ftp-group

``<username>`` is the django authentication username.

6. Run ``manage.py ftpserver`` command.

::

   $ python manage.py ftpserver 127.0.0.1:10021

7. Connect with your favorite FTP client.

Requirements
============

* Target Python version is 2.7, 3.4, 3.5, 3.6, 3.7
* Django>=1.11
* pyftpdlib
* six

License
=======

This software is licensed under the MIT License.

Documentation
=============

The latest documentation is hosted at Read The Docs.

https://django-ftpserver.readthedocs.org/en/latest/

Author
======

* Martin Nikolov

.. |docs| image:: https://readthedocs.org/projects/django-ftpserver/badge/?version=latest
   :target: https://readthedocs.org/projects/django-ftpserver/
.. |pypi| image:: https://badge.fury.io/py/django-ftpserver.svg
   :target: http://badge.fury.io/py/django-ftpserver
