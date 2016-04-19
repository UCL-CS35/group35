---
title: System Manual
last_updated: March 20, 2016
sidebar: mydoc_sidebar
permalink: /manuals/system/
---
### System Requirements

* Operating System: Mac OS X 10.7+, Ubuntu 14.04.4 x64 (Tested)

* Memory: 5GB+ (excluding memory space required for Raw and Processed Dataset)

* Browser: Chrome 45+, Safari 9+, Firefox 42+, Edge 25+, IE 11+ (JavaScript Enabled)

* Python and pip Installed

### Deploying INcDb

Install Virtual Environment using pip:

	pip install virtualenv

Cloning the app into a folder named "incdb-poc"

	git clone https://github.com/UCL-CS35/incdb-poc.git incdb-poc

Create the "incdb" virtual environment

	mkvirtualenv incdb

Install required Python packages

	cd /path/to/incdb-poc
	workon incdb
	pip install -r requirements.txt

### Setting Up INcDb

Run Celery Work

	celery worker -A app.initializers.mycelery -l info

Run Redis Server
	
	redis-server

To install redis-server from source on Ubuntu, follow the tutorial by Digital Ocean, <https://www.digitalocean.com/community/tutorials/how-to-install-and-use-redis/>

Initialising the Database

	# Setup Neruoysnth Dataset
	# Create DB tables and populate with Terms from Neurosynth
	# Populate the roles and users tables	
	python manage.py init_db

### Running the App
	
	# Start the Flask development web server
	./runserver.sh    # will run "python manage.py runserver"

Point your web browser to http://http://127.0.0.1:5000/

You can make use of the following users:

* email `jeremy@incdb.com` with password `Password1` with Administrative Privileges.
* email `ong@incdb.com` with password `Password1`.
* email `johnson@incdb.com` with password `Password1`.
* email `rajind@incdb.com` with password `Password1`.

### Testing the app

    # Run all the automated tests in the tests/ directory
    ./runtests.sh         # will run "py.test -s tests/"

### Known Issues

> Out of Memory during Installation of Python Packages

As `matplotlib` and `nilearn` both require a large memory space during installation, the remote server might run out of memory. One way to overcome this issue is to add Swap on the server. Swap is created from the hard drive space and used by the operating system to store data for a non-permanent basis when it run out memory in the RAM to hold the data.

If you face the Out of Memory issue, follow the tutorial by Digital Ocean to add Swap to your remote server. <https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-ubuntu-14-04>

> Trouble installing SciPy and NumPy

Try installing the dependencies of `python-scipy` and `python-numpy` using the following command:
	
	sudo apt-get build-dep python-numpy python-scipy

### Troubleshooting

* If you make changes in the Models and run into DB schema issues, delete the sqlite DB file `app.sqlite`.

* If you have any other troubles with setting up INcDb, tell us on the [Discussion Forum](../support/).