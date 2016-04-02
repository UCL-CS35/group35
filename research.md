---
layout: page
title: Research
permalink: /research/
---

This page details the research done by the group to understand the problem of the project and the suitable technologies required to build the solution.

## Background Research: NeuroVault & Neurosynth

![Neurovault](http://students.cs.ucl.ac.uk/2015/group35/images/neurovault.png "Neurovault")

There are two open source websites, NeuroVault and Neurosynth, that are widely used by neuroscience researchers. NeuroVault is a public repository for brain images supported by International Neuroinformatics Coordinating Facility, Max Planck Institute for Human Cognitive and Brain Sciences and Stanford University. Neurosynth is a platform that automate the process of producing functional magnetic resonance imaging (fMRI) data. Neurosynth process the data collected from numerous neuroimaging studies and does a meta-analysis on the coordinates in each study. The result is a images with a list of Terms that it is highly associated with.

As our client has developed a new study on capturing brain data while a person watch a movie, he want to build a public database that is similar to NeuroVault and Neurosynth. The database is a combination of both sites as it should allow users to interact with the brain image and view the list of Terms that it is highly associated with and at the same time allow other neuroscience researchers to upload their data for similar study

### Steep Learning Curve
As the 2 websites contain a high-level of technical details, we find that the learning curve to the use the website to be steep. It is important to keep in mind that our site should also be usable by the public with minimal technical knowledge, thus we will be replacing majority of the technical terms with simpler words.

### Open Source
Both websites are open sourced. Being open source allows other developers to contribute fixes and features to the application. It is an effective way of improving and maintaing a not-for-profit website.

## Version Control: Git & GitHub

We will be using Git for our version control system.

We shortlisted GitHub and Bitbucket as the possible options for hosting our project source codes. Bitbucket is an hosting service for Git repositories. It is attractive to small group (up to 5 members) who want to host their private projects online. GitHub is another hosting service provider but their free plan requires group to keep their code public. As our project's aim is to make a research study available to the public, our client has no objection on keeping the source code public. By having a public repository, interested developers can submit fixes or new features to improve INcDb. Lastly, GitHub is a also a better option for beginners like us as there is a huge community support available. We decided to use GitHub to host all our source codes and they are available at <https://github.com/UCL-CS35>.

We will be adopting Git Flow for our Git branching model. In our central repo, origin, we will have 2 main branches with infinite lifetime: master and develop. The origin/master always reflect a production-ready state. The origin/develop always reflect a state with the latest delivered development changes for the next release.

When origin/develop branch is ready to be release, all of the changes will be merged back into origin/master and then tagged with a release number. Each time when changes are merged back into origin/master, we will automatically build and roll-out our software to our production servers.

We will be using three supporting branches, namely Feature, Release, Hotfix branches. Feature branches may branch off from: develop, must merge back into: develop, has a branch naming convention: anything except master, develop, release-*, or hotfix-*. Feature branches are used to develop new features for the future release. Feature branches exist in developer repos only, not in origin.

## Web Framework: Python Flask

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

## Frontend Framework: Bootstrap

<table>
  <tbody>
  <tr>
    <th width="20%">Frameworks</th>
    <td width="40%"><a href="http://getbootstrap.com/">Bootstrap</a></td>
    <td width="40%"><a href="http://www.getmdl.io/">Material Design Lite</a></td>
  </tr>
  <tr>
    <th>Strength</th>
    <td>
      <ul>
        <li>Components include panel, popover, breadcrumb, thumbnails, inline alerts and wells.</li>
        <li>A lot of extensions and third-party widgets are available for Bootstrap </li>
        <li>Supports all the major browsers</li>
      </ul></td>
    <td>
      <ul>
        <li>Components include cards, mega footer, slider inputs and toggle switches</li>
        <li>No external dependencies</li>
        <li>Smaller file size</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Weakness</th>
    <td>
      <ul>
        <li><a href="https://jquery.com/">jQuery</a> dependency</li>
        <li>Need <a href="https://github.com/scottjehl/Respond">Respond.js</a> polyfill for CSS3 Media-queries support</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Follows stricter pattern of <a href="http://www.google.com/design/spec/">Material Design Concept</a></li>
        <li>Customisation might lead to a lost of the concept of Material Design</li>
        <li>Less number of extensions available</li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

We shortlisted Bootstrap and Material Design Lite for the front-end framework. We decided to use the Bootstrap framework, originally developed by Twitter, because Bootstrap allow a greater scale of customisation and is a mature framework that has extensive support available. With detailed documentation, it is easy to copy paste from the examples and get a usable result fast for Bootstrap.

Boostrap is an UI framework which provide a set of UI components for modern web application with the purpose of making it easy to build responsive websites. We can intergrate this framework into our appliation by adding its custom CSS and Javascript files into our application directory. This CSS and Javascript will be applied to the HTML elements with the pre-defined classes to acheive a standardised modern visual appearance.

## Neurosynth Viewer (Open Source)
Neurosynth Viewer is a CoffeeScript/JS library for visualization of functional MRI data. It provides us with a simple tools to display the brain scan image and navigation sliders to surf through a single plane. The documentation of the library is extensive and easy to implement.

* Demo: <http://pilab.psy.utexas.edu/demos/nsviewer/index.html>
* Source: <https://github.com/neurosynth/nsviewer>

## Deployment
As our web application will be using the Python Flask Framework, the deployment server/service we will be using must support Python Flask applications. To deploy our web application, we could use a server provided by UCL or a cloud service.

1. If we do use a local server, there are several advantages. Firstly, we do not need to purchase subscriptions for the cloud services, and may have less restrictions.
2. Heroku is one of the cloud services which we found to support Python Flask web applications. It provides easy deployment methods such as simply pushing from a Git repository, then automatically compiles and run the application.
3. Similarly, Digital Ocean also supports Python Flask, with their main feature being speed, they supply cloud servers running with solid state drives, so data access would be faster. In addition, they give a choice of a magnitude of Linux distributions to be installed on the server.
4. Microsoft Azure is another cloud hosting platform which may be considered. One of its features is the access to a large number of APIs, connecting to other services is easier. It also supports "continuous integration", so pushes to GitHub can be automatically built, tested and deployed.

As our client does not have any prior knowledge of the deployment services available, he requested the group for a summary of the services. We researched on the three services, Heroku, Digtial Ocean and Microsoft Azure and comipled the information into the table below.

<table class="table table-striped table-bordered">
    <thead>
    <tr>
      <th>Heroku-Free</th>
      <th>Heroku-Hobby</th>
      <th>Digital Ocean - 1TB Transfer</th>
      <th>Microsoft Azure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <ul>
          <li>Sleep after 30 minutes of inactivity</li>
          <li>Must sleep 6 hours in a 24 hour period</li>
          <li>Custom Domains</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Never sleeps</li>
          <li>Multiple workers for more powerful apps</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>512MB Memory</li>
          <li>Single-core processor</li>
          <li>20GB SSD</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Shared Cores</li>
          <li>500MB RAM</li>
          <li>1GB Storage</li>
          <li>2GB SQL Database</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>At zero cost</li>
          <li>Great tools for deployment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Great tools for deployment</li>
          <li>Troubleshoot materials widely available</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Have control over virtual machine</li>
          <li>Well-designed tutorials to setup environment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Free student version</li>
          <li>Reliable provider</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Not available at all times</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Don't have total control over deployment process</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Require user to setup environment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Confusing pricing model</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://www.heroku.com/pricing">https://www.heroku.com/pricing</a>
      </td>
      <td>
        <a href="https://www.heroku.com/pricing">https://www.heroku.com/pricing</a>
      </td>
      <td>
        <a href="https://www.digitalocean.com/pricing/">https://www.digitalocean.com/pricing/</a>
      </td>
      <td>
        <a href="https://azure.microsoft.com/en-gb/pricing/">https://azure.microsoft.com/en-gb/pricing/</a>
      </td>
    </tr>
    <tr>
      <td>Free</td>
      <td>£4.65 ($7) per month</td>
      <td>£3.32 ($5) per month</td>
      <td>£5.91 per month</td>
    </tr>
  </tbody>
</table>

We reach an agreement with our client to select Heroku. We choose Heroku because it offer a Free plan that will reduce the cost required during the development stage. As Heroku also provide a url for the web application deployed on the free plan, our client dose not need to purchase the domain name before INcDb is ready to go live. The restriction of 6 hours of downtime is not critical during the development stage too.