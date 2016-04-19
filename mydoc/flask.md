---
title: Flask
tags: 
keywords:
last_updated: March 20, 2016
sidebar: mydoc_sidebar
permalink: /research/flask/
toc: false
---

Our client requested the group to build a website similar to the one found on Neurosynth which uses the web framework, Python Flask. Our group decided to select Flask as our framework as we try to emulate a repository similar to Neurosynth. By using Flask, which is written in Python, it allows the group to learn more about Python, which is also the language for most of the tools that are used to process the collected brain images.

Flask is a Python micro web framework based on Werkzeug and Jinja2 (<http://flask.pocoo.org/>), that has a file structure (<http://damyanon.net/flask-series-structure/>) that contains a folder named bin – contains scripts that will be executed on the command line, a folder named docs – contains project related documentation files, a folder named tests – contains unit tests, a folder named `[app-name]` – contains the application itself, and a file named `run.py` – used to run the Flask application.

Inside the application folder, there will be different modules as the application is configured to be modular, based on the blueprint concept in Flask. Inside each module folder, there will be a `_init_.py` file which initialize the folder as Python package. These modules will be register by using the method `app.register_blueprint([module-name], url_prefix='/')` in the application object, `[app-name]/_init_.py`.

## Flask Extensions

In order to speed up our development process, we will be using a few Flask Extensions, which are Python packages that add new function to the Flask app.

| __Name__       		| SQLAlchemy (via Flask-SQLAlchemy)	|
| __Description__ 	| An SQL toolkit for database access and is well-known for its object relational mapper.	|
| __Strength__    	| Enterprise-level persistence patterns, efficient and high-performing database access.	|
| __Weakness__    	| Integrating with legacy systems is challenging.	|

| __Name__       		| Flask-User	|
| __Description__ 	| An user account management for Flask that include register, confirmation email, login and others. 	|
| __Strength__    	| Reliable, well-documented and ready to use.	|
| __Weakness__    	| The extension is still in Beta release.	|

| __Flask-Migrate__	| SQLAlchemy database migrations for Flask applications using Alembic	|
| __Flask-WTF__ 	| Simple integration of Flask and WTForms, including CSRF, file upload and Recaptcha integration	|
| __Flask-Uploads__	| A Flask extension to help you add file uploading functionality to your site.	|
| __Flask-Mail__	| Flask-Mail adds SMTP mail sending to your Flask applications	|