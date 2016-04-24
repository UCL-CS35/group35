---
title: Design Patterns
sidebar: mydoc_sidebar
permalink: /development/design-patterns/
---

## Model View Controller (MVC)

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

## Decorators

We used Decorator design pattern to add additional functionality to each view in Flask. A decorator is a function that returns a function. As each view in Flask is a function, we used the `route()` and `login_required()` decorators to implement routing and access control for the views.

### `route()` decorator

`route()` is a decorator by Flask that is used to register the a view function for a given URL rule. Using a decorator simplify the code as it apply the routing functionality to the view function that follows it. Although the `flask.add_url_rule()` work exactly the same, it requires the name of view function in its parameter. A change in the name of the view function will result in error in routing. 

### `login_required()` decorator

To allow only logged in user to create collection and upload Raw Dataset, we apply the `@login_required` decorator provided by Flask-Login to redirect user to the login in page if they are not logged in and try to access the page.

The following code snippets show how `route` and `login_required` decorators are implemented.

    @contribute_blueprint.route('contribute/new', methods=["POST", "GET"])
    @login_required  # Limits access to authenticated users
    def new_collection():
        """ Allow user to create new collection """

        ...