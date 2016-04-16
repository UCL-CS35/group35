---
layout: page
title: Docs
permalink: /docs/
---

TODO 

4. Development plan, iterations and forks in prototypes
5. Architectural diagrams
6. Technical achievements, implementation details, use of design patterns
8. Referenced materials cited and examples/trials made
9. Testing and evaluation of the product solution

## System Manual

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


<hr>

## User Guide v0.1

### Repository Browsing

> Select a Movie

From the Home page or the Movies index page, you can select a Movie by looking through the list of recently added Movies to the website. Once you select a Movie, you can browse through the different Terms and Components (brain images) available for the selected Movie.

> Search for a Movie

From the home page or the Movies index page, you can search for a specific Movie by using the search bar. An auto-suggestion box will assist your search with relevant Movie suggested based on your input. Once you select a Movie, you can browse through the different Terms and Components (brain images) available for the selected Movie.

> Select a Term

From the Terms index page, you can select a Term by looking through the list of Term that has at least one Component that is highly-coreleated with. Once you select a Term, you can browse throught the different Components corelated with the selected Term. 

> Search for a Term

From the Terms index page, you can search for a specific Term by using the search bar. Once you select a Term, you can browse throught the different Components corelated with the selected Term. 

> View Brain Component

From the selected Movie or Term page, you can select a Component to futher investigate the brain images. For each Component, the Neurosynth's Brain Viewer display 3 brain images (the x-axis, y-axis and z-axis). You can click around different points on the brain image or use the sliders below each image to adjust the coordinates.

Below the set of brain images consists the layers displayed. These usually comprise of the brain overlay as a template and the remaining layers relevant to the different regions. When browsing through brain imagery for different Terms, you might notice layers that comprise of “forward” and “backward” analysis. What exactly are they? To simply put -

* Forward Analysis - z-scores corresponding to the likelihood that a region will activate if a Movie uses a particular Term

* Backward Analysis - z-scores corresponding to the likelihood that a Term is used in a Movie given the presence of reported activation

### Data Submission

**Only signed-in user can submit dataset**

> Create Collection

You can create a Collection by filling up the information of the Collection. The Collection Name and Movie Name are required for the creation of the Collection. You can fill in the non-mandatory fields later. 

> Upload Raw Dataset

After creating the Collection, you will be redirected to the Upload page. You can upload your raw dataset in one or multiple compressed files. The accepted file formats are zip and tar.gz. The compressed file must contain the brain images in the immediate child directory. A progress bar will indicate the uploading progress. A warning dialog will be displayed if you attempt to navigate away from the upload page during the uploading process. As the size of the files are big, please wait patiently for the files to be uploaded.

> Edit Collection

You can edit the Collection's details on the Collection page. The Collection Name is an unique indentifier for the Collection so it cannot be edited.

> Delete Collection

You can delete the Collection and the Raw Dataset that you uploaded will be removed from the INcDb's server. If the Processed Dataset is uploaded for the deleted Collection, the Processed Dataset will also be removed.

### User Management

> Register Account

You can register an account by entering your Email, Title, First and Last Name. You are required to set your password for your account and retype the same password for confirmation. After successful registration, you can sign in to INcDb with your email and password.

> Sign In and Sign Out

If you already has a registered account, you can sign in to INcDb with your email and password. To sign out from INcDb, click on your name on the navigation bar and click on the Sign Out link.

> Edit User Account

If you are signed in to INcDb, you can edit your account's details such as your Title, First and Last Name, and Affiliation. To update your account with the changes you made, you must click on the Save button. You can also change your password. 

### Administrative Privileges

> Download user uploaded Raw Dataset

As administrator of INcDb, you can download the Raw Dataset of a Collection, uploaded by the other users. You will download a compressed file containing all the brain images of the Collection you had chosen. As the the size of the brain images are large, please wait patiently for the download to be completed.

> Upload Processed Dataset

As administrator of INcDb, you can upload the Processed Dataset of a Collection that is created by other users. When the upload is completed, a background thread will decode the brain images and compute their corelations with the Terms in the database. The database will be populated with the Components (brain images) and the corelations will be stored in a text file on the server.


