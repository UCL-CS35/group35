---
title: Trials
sidebar: mydoc_sidebar
permalink: /development/trials/
---

## Accessing Database with Celery

At first we thought reading and writing of the SQLite database using background tasks would be done in the same manner as non background tasks, but it failed to gain access to the existing database, returning with error messages like 'no such table'.

To try and solve that problem we looked into how Neurosynth uses Celery for their background tasks and found that they created a subclass of Celery Tasks - namely NeurosynthTask. However, the attempt did not result in the background task successfully reading and writing the database. 

Then from further researching online, we found a solution which uses a new database session for background tasks. In addition to creating a scoped session for the background task, we also had to create a new sublass of Celery Tasks - 'SqlAlchemyTask' which removes the session at the end of the task to ensure a closed connection. 

## Implementing Neurosynth Viewer

The initial problem that surfaced was to how web pages that consisted of the Neurosynth Viewer were dynamically created depending on the Term/Component selected. This presented a challenge on how we could feed the location of the relevant Component to the Viewer script in order to load the correct brain images

What made part of the implementation easy for us was Flask’s ability to generate macro fields to add Python functions within the HTML code that provided the location of the brain images for the relevant page. This made it easy to embedded within the Javascript code for the Viewer.

One issue we had in particular was loading specific brain images that were in 64-bit format, which had an incompatibility issue with the Viewer. This was resolved by regenerating the Viewer code using the CoffeeScript libraries provided by the GitHub repository.

Another particular issue we had was the brain image generation on Terms for an individual Movie. This involved the process of merging relevant brain images into one.

Our initial approach for this was to use an FSL interface to merge brain images into a 4D brain image. However this still rose incompatibility issues with the Viewer. This was later resolved with our client recommending the AFNI interface to merge the brain images into one that can be read by the viewer.

## Deployment: Heroku vs Digital Ocean

Based on the research done in COMP204P, we recommended and agreed with our client to deploy the demo version of INcDb on the Heroku platform.

However during the deployment of INcDb, we discover that Heroku does not have persistant storage and is unable to install required Python packages like SciPy and NumPy.

- We manage to resolve the issue with persistant storage by storing the uploaded dataset on Amazon S3.

- We tried installing different type of custom Heroku buildpack for Python, Numpy, and Scipy without success.

In the end, we decided to deploy INcDb on [Digital Ocean](https://www.digitalocean.com/) instead as it is a remote Linux machine and we will have the full root access to the machine. The root access allow us to install all the required Python packages. Having a remote machine with 20GB also allows us to move the storage to the machine and remove the reliance on a third party storage server. However as each dataset usually contains more than 1GB of brain images, we will recommend our client to use Amazon S3 as the storage server when the website goes into production.