Flask
=====

Flask is a lightweight `WSGI`_ web application framework. It is designed
to make getting started quick and easy, with the ability to scale up to
complex applications. It began as a simple wrapper around `Werkzeug`_
and `Jinja`_ and has become one of the most popular Python web
application frameworks.

Flask offers suggestions, but doesn't enforce any dependencies or
project layout. It is up to the developer to choose the tools and
libraries they want to use. There are many extensions provided by the
community that make adding new functionality easy.

Key features of Flask include:
====
Routing: Flask allows you to define routes, which are URLs that the 
application can handle. You can associate each route with a Python 
function, making it easy to execute specific code when a user accesses a 
particular URL.

Templates: Flask uses Jinja2 templates for rendering dynamic content in 
HTML. This allows you to create dynamic web pages by embedding Python 
code within your HTML templates.

Web Server Gateway Interface (`WSGI`): Flask is based on the WSGI standard, 
making it compatible with various web servers. This flexibility allows 
you to deploy Flask applications in different environments.

Extension Support: Flask follows a minimalist approach but allows you to 
extend its functionality by using various extensions. These extensions 
cover a wide range of features, from handling forms to integrating with 
databases.

.. _WSGI: https://wsgi.readthedocs.io/
.. _Werkzeug: https://werkzeug.palletsprojects.com/
.. _Jinja: https://jinja.palletsprojects.com/


Installing
====
Python Version
-----
We recommend using the latest version of Python. Flask supports Python 3.8 and newer.

Virtual environments
-----
Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects 
you have, the more likely it is that you need to work with different 
versions of Python libraries, or even Python itself. Newer versions of 
libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for 
each project. Packages installed for one project will not affect other 
projects or the operating system’s packages.

Python comes bundled with the `venv`_ module to create virtual environments.

.. _venv: https://docs.python.org/3/library/venv.html#module-venv

Create an environment
-----
Create a project folder and a .venv folder within:

For macOS/Linux:
::
    $ mkdir myproject
    $ cd myproject
    $ python3 -m venv .venv

For Windows: 
::
    > mkdir myproject
    > cd myproject
    > py -3 -m venv .venv

Activate the environment
-----
Before you work on your project, activate the corresponding environment:

For macOS/Linux:
:: 
    $ . .venv/bin/activate

For Windows: 
::
    > .venv\Scripts\activate

Your shell prompt will change to show the name of the activated environment.

Install Flask
-----
Within the activated environment, use the following command to install Flask:
::
    $ pip install Flask
Flask is now installed

.. Install and update using `pip`_:

.. .. code-block:: text

..     $ pip install -U Flask

.. .. _pip: https://pip.pypa.io/en/stable/getting-started/


A Simple Example
----------------

.. code-block:: python

    # save this as app.py
    from flask import Flask

    app = Flask(__name__)

    @app.route("/")
    def hello():
        return "Hello, World!"

.. code-block:: text

    $ flask run
      * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)


Contributing
------------

For guidance on setting up a development environment and how to make a
contribution to Flask, see the `contributing guidelines`_.

.. _contributing guidelines: https://github.com/pallets/flask/blob/main/CONTRIBUTING.rst


Donate
------

The Pallets organization develops and supports Flask and the libraries
it uses. In order to grow the community of contributors and users, and
allow the maintainers to devote more time to the projects, `please
donate today`_.

.. _please donate today: https://palletsprojects.com/donate


Links
-----

-   Documentation: https://flask.palletsprojects.com/
-   Changes: https://flask.palletsprojects.com/changes/
-   PyPI Releases: https://pypi.org/project/Flask/
-   Source Code: https://github.com/pallets/flask/
-   Issue Tracker: https://github.com/pallets/flask/issues/
-   Chat: https://discord.gg/pallets
