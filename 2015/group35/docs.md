---
layout: page
title: Docs
permalink: /docs/
---

## Development Plan

The development of INcDb is done based on the features specified sequentially.

1. User Management 
2. Neurosynth Dataset generation
3. Database design
3. Computation of correlation between Component and Terms
4. Repository Browsing
5. Data (Raw Dataset) Submission by User
6. Implement Front-End Design based on Mockup agreed with Client
7. Neurosynth Viewer to display brain images
8. Use Celery and Redis to move Decoding function to background task
9. Unit Tests

### Iterations

__Iteration #1 - User Management__

The first iteration of INcDb is the prototype done for COMP204P in Term 1. The app used Flask-User to implement the user management feature. We used the Flask-User starter app as the base and modify the code to suit our the project requirements. We changed the details of the default account and added extra fields like 'Title' and 'Affiliation'. 

__Iteration #2 - Neurosynth Dataset generation, Database design, Computation of correlation between Component and Terms, Repository Browsing__

The second iteration include adding the Neurosynth Dataset to the application, developing the database structure, implemeting the decoding function and basic repository browsing capability. This iteration include multiple features that are interconnected. The dataset and database was necessary for the decoding function to work and the repository browsing is included in this iteration to ensure that the database structure is well designed. 

Although we can use database query to check that the decoding function insert data to the database as designed, adding the repository browsing can help us improve the database design so that the query to retreive the necessary data will be kept simple.


__Iteration #3 - Data (Raw Dataset) Submission by User__

With the user management implemented in Iteration #1, we added the ability to upload data for signed in user. During this iteration, we added a new table, `Collections`, to the database and a `uploads` folder to the application to store the Raw Dataset uploaded by the user. We also implemented a progress bar to inform user of the upload process. 

__Iteration #4 - Front-End Design__

As the basic features of the application is mostly completed, we started to implement the front-end design based on the agreed mockup on the application during this iteration. We make changes to the original the mockup based on the feedback from our client and TA. The changes include capitalising the first letter to improve the professionalism of the site and increase the font-size of the body text to improve readability.

__Iteration #4 - Neurosynth Viewer__

With the design in place, we started working on adding the Neurosynth Viewer to the application. The Neurosynth Viewer is a tool to display the brain images with sliders to interact with the images. We also added the merging function during this iteration. The merging function combines all the brain images (Component) of the Movie for a specific Term and display them using the Neurosynth Viewer.
 
__Iteration #5 - Moving decoding funtion to a background task___

During this iteration, we move the decoding function to a backgroun task. As the decoding function compute the correlations between each Component uploaded and each Term in the database, it take a long time to complete. It is not feasible to get our Client to wait for both the uploading and the decoding. Hence, we used a background task to run the process and our Client can carry on managing the application after uploading the Processed Dataset.

__Iteration #6 - Unit Tests__

The final iteration of INcDb include the testing the application using basic unit test cases. For details of the testing, please refer to the Testing page.

## Technical Achievements

### Implementation Details

1. Neurosynth Dataset generation. 
    
    INcDb requires a Neurosynth dataset that it uses to generate Term Analyses. The generation of Neurosynth Dataset is a memory-intensive operation which is not suitable to be done on a remote server, which typically has less RAM. 

    We suggest the Dataset to be generated on a local machine. Follow the instructions on <https://github.com/neurosynth/neurosynth> to build your own Dataset (`neurosynth_dataset.pkl`) and copy the Dataset to `incdb-poc/app/data/assets/`.

    With the Dataset in place, we can initialise the database and add the Analyses to the database. These analyses will then be used to compute the correlation of the Components with the Terms.

2. Flask Application
		
    The main function of the INcDb is the repository browsing. This is implemented using database query and Flask routing mechanism. Flask routing function help to pass variable name through the URL and this variable is used to select the necessary data from the database to be displayed. 

    The user management was implemented using the Flask extension - Flask-User. The user management allow signed in users to create Collection and upload Raw Dataset. 

    Flask-WTF, a Flask extension, was used to simplify the creation of the complicated Collection's form. 

3. Computation of correlation between Component and Terms
   
    Another key function performed by the INcDb is to compute the correlations of the Components uploaded by our client with the Terms Analyses generated by the Neurosynth Dataset generation. As requested by our client, we referenced the computation done by the open-sourced Neurosynth-Web, <https://github.com/neurosynth/neurosynth-web/blob/master/nsweb/tasks/__init__.py>, and implemented a similar decoding function for INcDb.

    The decoding is done when new Processed Dataset is uploaded to the server by our client and the top 10 Terms (with the highest correlations) for each Component are stored in a text files on the remote server. These text files are retrieved to display the correlation values when user view the Component.

    For each Component of the Processed Dataset, a row in the Decodings table (in the database) is also created and tagged with the Term that it has the higest correlation with.

4. Neurosynth Viewer
   
    (Explain setup, selection of Components, merging)

5. Background task using Celery and Redis

    (Explain how is it move to backgound, starting celery workers, running redis server)

### Dependencies

The application is developed with a list of dependecies. The complete list of Python packages dependencies can be found at <https://github.com/UCL-CS35/incdb-poc/blob/master/requirements.txt>.

We will like to highlight a few key dependencies that were critical for the development of INcDb.

<table>
	<thead>
		<tr>
			<th>Name</th>
			<th>Role</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td width="15%">Flask</td>
			<td>The micro-framework that INcDb runs on.</td>
		</tr>
		<tr>
			<td>Flask-User</td>
			<td>Flask extension used to implement User Management feature.</td>
		</tr>
		<tr>
			<td>Flask-WTF</td>
			<td>Flask extension used to simply form creation.</td>
		</tr>
		<tr>
			<td>Neurosynth</td>
			<td>Neurosynth is used to generate analyses that is used for the decoding of the Processed Dataset uploaded by our client.</td>
		</tr>
		<tr>
			<td>gunicorn</td>
			<td>A Python WSGI HTTP Server to serve the Flask application.</td>
		</tr>
		<tr>
			<td>celery</td>
			<td>A task processing system used to manage background tasks like decoding.</td>
		</tr>
		<tr>
			<td>Redis</td>
			<td>Redis is used as message broker to pass messages between Flask application and Celery workers.</td>
		</tr>
	</tbody>
</table>

### Code Structure

The application first-level code structure is presented below and the role of each file or folder is explained.

* incdb-poc/
    * app/
        * Contains Models, Views (templates), Controllers, Static files (CSS, JS, Images, Fonts), Setup scripts
    * data/
        * Contains Neurosynth Dataset, Decoding results, Admin uploaded Processed Dataset, Generated memmaps, FAQ data
    * default/
    * docs/
        * Documentations generated by Sphinx
    * migrations/
    		* Migrations genereted (Currently empty)
    * node_modules/
        * Node modules required to run Neurosynth Viewer
    * src/
        * Coffeescript requred to run Neurosnyth Viewer
    * tests/
        * pytests written to test User Managemnent, Search, Creation of Collection
    * uploads/
        * Contains User uploaded Raw Dataset
    * .gitignore
        * Ignore Database and Data folders 
    * Aptfile
    * Cakefile
    * Guardfile
    * LICENSE.txt
    * manage.py
        * Use to start the Flask application
    * README.md
    * requirements.txt
        * List of Python packages required
    * runserver.sh
        * Bash script to run the the Flask application in development mode
    * runtests.sh
        * Bash script to run the Test Cases in /tests folder
    * supervsiord.conf
        * Supervisor configuration file used for Deployment

For the complete code, you can view them on [GitHub](https://github.com/UCL-CS35/incdb-poc). 

## Design Patterns

### Model View Controller (MVC)

For INcDb, we implemented Model View Controller to separate the application logic from the user interface. The separation is done by using the Controller to receive input and interacting with the Model and passing the required data to the View.

The **Controllers** are found in the path `app/controllers`. Each actions in the `controllers` are associated with a predefined route. The controller action uses the **Models** found in `app/models` to retrieve data from a database. The data is then passed to a **View**, located in the `app/templates/`. The view will then present the data to the user in their browser.

Example of a Controller action:

	@home_blueprint.route('guide')
	def guide():
	    return render_template('guide.html')

Example of a Model:

	class DecodingSet(db.Model):
      __tablename__ = 'decoding_set'

      id = db.Column(db.Integer, primary_key=True)
      analysis_set_id = db.Column(db.Integer,
                                db.ForeignKey(AnalysisSet.id), nullable=True)
      analysis_set = db.relationship(AnalysisSet,
                                   backref=db.backref('decoding_set'))
      name = db.Column(db.String(20))
      n_images = db.Column(db.Integer)
      n_voxels = db.Column(db.Integer)
      is_subsampled = db.Column(db.Boolean)

### Decorators

We used Decorator design pattern to add additional functionality to each view in Flask. A decorator is a function that returns a function. As each view in Flask is a function, we used the `route()` and `login_required()` decorators to implement routing and access control for the views.

> `route()` decorator

`route()` is a decorator by Flask that is used to register the a view function for a given URL rule. Using a decorator simplify the code as it apply the routing functionality to the view function that follows it. Although the `flask.add_url_rule()` work exactly the same, it requires the name of view function in its parameter. A change in the name of the view function will result in error in routing. 

> `login_required()` decorator

To allow only logged in user to create collection and upload Raw Dataset, we apply the `@login_required` decorator provided by Flask-Login to redirect user to the login in page if they are not logged in and try to access the page.

The following code snippets show how `route` and `login_required` decorators are implemented.

	@contribute_blueprint.route('contribute/new', methods=["POST", "GET"])
	@login_required  # Limits access to authenticated users
	def new_collection():
	    """ Allow user to create new collection """

	    ...

<hr>

## Architectural Diagrams

### Deployment Diagram
<object data="../images/diagrams/deployment.svg" width="100%" type="image/svg+xml">
</object>

Database Schema
<img src="../images/diagrams/schema.svg" style="width:100%">

<hr>

## Referenced Materials

Referenced materials cited and examples/trials made

1. neurosynth-web - <https://github.com/neurosynth/neurosynth-web>

2. Neurosynth Viewer - <https://github.com/neurosynth/nsviewer>

3. Flask-User starter app - <https://github.com/lingthio/Flask-User-starter-app>

4. Helper to list routes (like Rails' rake routes) - <http://flask.pocoo.org/snippets/117/>

5. How to paginate in Flask-SQLAlchemy for db.session joined queries? - <http://stackoverflow.com/questions/15727155/how-to-paginate-in-flask-sqlalchemy-for-db-session-joined-queries>

6. Error Handlers - <http://flask.pocoo.org/docs/0.10/patterns/errorpages/#error-handlers>

7. Flask AJAX Autocomplete - <http://stackoverflow.com/questions/15310644/flask-ajax-autocomplete>

8. flask-multi-upload - <https://github.com/kirsle/flask-multi-upload>

9. How to unzip file in Python on all OSes? - <http://stackoverflow.com/questions/12886768/how-to-unzip-file-in-python-on-all-oses>

10. Setting up Celery Task Queue - <http://docs.celeryproject.org/en/latest/index.html>

11. Running Celery Worker Daemonized using Supervisor - <https://github.com/celery/celery/blob/3.1/extra/supervisord/celeryd.conf>

12. Accessing DB for Celery Tasks - <http://www.prschmid.com/2013/04/using-sqlalchemy-with-celery-tasks.html>

11. !!! NSViewer

### Trials Made

Accessing DB with Celery

- At first we thought reading and writing of the SQLite database using background tasks would be done in the same manner as non background tasks, but it failed to gain access to the existing database, returning with error messages like 'no such table'.

- To try and solve that problem we looked into how Neurosynth uses Celery for their background tasks and found that they created a subclass of Celery Tasks - namely NeurosynthTask. However, the attempt did not result in the background task successfully reading and writing the database. 

- Then from further researching online, we found a solution which uses a new database session for background tasks. In addition to creating a scoped session for the background task, we also had to create a new sublass of Celery Tasks - 'SqlAlchemyTask' which removes the session at the end of the task to ensure a closed connection. 

<hr>

## Testing and Evaluation

### Unit Tesing using pytest

We tested INcDb on 2 different kind of test cases. 

1. The first kind is using the client which act like the browser, to navigate INcDb. We check that given each URL, the expected layout is return by confirming the content of the layout contain the keywords (usually the title of the page) we specified.

2. We also tested the Python functions like `find_or_create_user` to verify that data is added correctly into the database.

The set of test cases can be found at <https://github.com/UCL-CS35/incdb-poc/tree/master/tests>

### Issues Faced

As we try to keep each set of test cases independent, we intialise the database for every set of test cases. However, the initialisation of Neurosynth dataset take up a considerable amount of time (at least 5 minutes). Thus, we did not implement detailed and complicated test cases.

<hr>

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


