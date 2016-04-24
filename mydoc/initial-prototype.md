---
title: Initial Prototype
tags: 
keywords:
sidebar: mydoc_sidebar
permalink: /research/prototype/
---

## System Overview


![System Overview]({{ "/images/research/system-overview.png" | prepend: site.baseurl }})

## Initial Prototype (COMP204P)

Our prototype for COMP204p is an Flask application, INcDb User. The application is based on the Flask-User-starter-app as we will be using the Flask extension, Flask-User, to implement our user management functionality. The source code of the INcDb User is on <https://github.com/UCL-CS35/incdb-user>.

### Add Relevant Fields
Beside the basic user management functionality from the starter app, we added 2 new fields, title and affiliation to reflect our project requirements.

### Support latest version Flask-User
As the starter-app is dependent on an older version of Flask-User, we updated the code to support the latest version of Flask-User.

### Unit Testing
We also introduce test cases to experiment with pytest, our selected testing tool. See Testing Strategy for more information about testing.

### Screenshots
![Home Page]({{ "/images/research/homepage.png" | prepend: site.baseurl }})

![No Permission]({{ "/images/research/nopermission.png" | prepend: site.baseurl }})

![Sign In]({{ "/images/research/signin.png" | prepend: site.baseurl }})

![Signed In]({{ "/images/research/signedin.png" | prepend: site.baseurl }})

### Setup

Install Virtual Environment using pip:

	pip install virtualenv

Cloning the app

	mkdir INcDb
	cd INcDb
	git clone https://github.com/UCL-CS35/incdb-user.git incdb-user

Create the 'incdb-user' virtual environment

	mkvirtualenv incdb_user_env

Install required Python packages

	cd /path/to/incdb-user
	workon incdb_user_env
	pip install -r requirements.txt

Configuring the app
Copy the app/env_settings_example.py to an env_settings.py that resides outside the code directory and point the OS environment variable ENV_SETTINGS_FILE to this file.

	# Copy env_settings.py and place it outside of the code directory
	cd /path/to/project
	cp app/env_settings_example.py ../env_settings.py

	# Point the OS environment variable `ENV_SETTINGS_FILE` to this file
	export ENV_SETTINGS_FILE=/path/to/env_settings.py
	Before deploying this application, we will have to configure the database URL and SMTP account that will be used to access the database and to send emails.

Initializing the Database

	# Create DB tables and populate the roles and users tables
	python manage.py init_db

Running the app

	# Start the Flask development web server
	./runserver.sh    # will run "python manage.py runserver"

Point your web browser to http://localhost:5000/

You can make use of the following users:

* email user@example.com with password Password1.
* email admin@example.com with password Password1.

### Data Model for INcDb User


#### Users Table
<div class="table-responsive">
<table class="table table-striped table-bordered">
  <thead>
    <tr>
      <th>id</th>
      <th>email</th>
      <th>confirmed_at</th>
      <th>password</th>
      <th>reset_password_token</th>
      <th>active</th>
      <th>first_name</th>
      <th>last_name</th>
      <th>title</th>
      <th>affiliation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>
</div>

#### Roles Table

<div class="table-responsive">
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>id</th>
        <th>name</th>
        <th>label</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </tbody>
  </table>
</div>


#### User Roles Table

<div class="table-responsive">
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>id</th>
        <th>user_id</th>
        <th>role_id</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </tbody>
  </table>
</div>

### Dependency for INcDb User

<div class="table-responsive">
<table class="table table-striped table-bordered">
  <thead>
    <tr>
      <th>Flask Framework</th>
      <th>Flask Extensions</th>
      <th>Development Tools</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Flask</td>
      <td>
        Flask-Migrate<br>
        Flask-SQLAlchemy<br>
        Flask-User<br>
        Flask-WTF
      </td>
      <td>
        pytest<br>
        pytest-flask<br>
        pytest-cov<br>
        selenium
      </td>
    </tr>
  </tbody>
</table>
</div>