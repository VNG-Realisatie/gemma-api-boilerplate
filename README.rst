{% comment %}

===============
Getting started
===============

Below you'll find the steps to create a Django project from scratch, using the
VNG boilerplate template. The ``<project_root>`` is typically placed in
your home directory or ``/srv/sites/``. It can be named anything but typical
examples are ``corporate``, ``website`` or more specific like
``acme-website``:

.. code-block:: bash

    $ mkdir <project_root>
    $ cd <project_root>

Create the virtual environment that holds your copy of Python and relevant
libraries:

.. code-block:: bash

    $ virtualenv env or virtualenv --python=/usr/bin/python3.6 env
    $ source env/bin/activate
    $ pip install django<2.1

Start a new Django project, named ``<project_name>``, using the template. It
can be usefull to use a ``<project_name>`` that serves as namespace in your
code, like ``vng``:

.. code-block:: bash

    $ django-admin startproject --template=https://github.com/VNG-Realisatie/gemma-api-boilerplate/archive/master.zip --extension=env,py,rst,html,gitignore,dockerignore,json,js,sh,cfg,yml,Dockerfile <project_name> .

You'll need pip-compile to generate the pinned versions of the requirements:

.. code-block:: bash

    $ pip install pip setuptools --upgrade (optionally)
    $ pip install pip-tools
    $ ./bin/compile_dependencies.sh

Modify the ``README.rst`` to be suitable for this project.

Once the project is ready, create a repository online and commit the files to
the repository:

.. code-block:: bash

    $ git init
    $ git remote add origin git@github.com:VNG-Realisatie/<repo>.git
    $ git add --all
    $ git commit -m ":tada: Initial project layout."
    $ git push --set-upstream origin develop

You'll now have a starting point for your new project. Continue to the
installation instructions below and start at step 3.

To start the project, you can continue to the Installation section, bullet 3.

**NOTE:** The section above will not be included in your project's README.
Below you'll see the actual project README template.


{% endcomment %}========================

========================

:Version: 0.1.0
:Source: https://github.com/VNG-Realisatie/gemma-{{ project_name|lower }}
:Keywords: zaken, zaakgericht werken, GEMMA
:PythonVersion: 3.6

|build-status|

Referentieimplementatie van de {{ project_name }} (ABBREVIATION).

Inleiding
=========

``<describe the project in a few paragraphs and briefly mention the features>``

Deze component heeft ook een `testomgeving`_ waar leveranciers tegenaan kunnen
testen.

Documentatie
============

Zie ``INSTALL.rst`` voor installatieinstructies, beschikbare instellingen en
commando's.

Indien je actief gaat ontwikkelen aan deze component raden we aan om niet van
Docker gebruik te maken. Indien je deze component als black-box wil gebruiken,
raden we aan om net wel van Docker gebruik te maken.

Referenties
===========

* `Issues <https://github.com/VNG-Realisatie/gemma-{{ project_name|lower }}/issues>`_
* `Code <https://github.com/VNG-Realisatie/gemma-{{ project_name|lower }}>`_


.. |build-status| image:: http://jenkins.nlx.io/buildStatus/icon?job=gemma-{{ project_name|lower }}-stable
    :alt: Build status
    :target: http://jenkins.nlx.io/job/gemma-{{ project_name|lower }}-stable

.. |requirements| image:: https://requires.io/github/VNG-Realisatie/gemma-{{ project_name|lower }}/requirements.svg?branch=master
     :target: https://requires.io/github/VNG-Realisatie/gemma-{{ project_name|lower }}/requirements/?branch=master
     :alt: Requirements status

.. _testomgeving: https://ref.tst.vng.cloud/ABBREVIATION/

Licentie
========

Copyright © VNG Realisatie {% now "Y" %}

Licensed under the EUPL_

.. _EUPL: LICENCE.md
