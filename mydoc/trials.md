---
title: Trials
last_updated: March 20, 2016
sidebar: mydoc_sidebar
permalink: /development/trials/
---

## Accessing Database with Celery

- At first we thought reading and writing of the SQLite database using background tasks would be done in the same manner as non background tasks, but it failed to gain access to the existing database, returning with error messages like 'no such table'.

- To try and solve that problem we looked into how Neurosynth uses Celery for their background tasks and found that they created a subclass of Celery Tasks - namely NeurosynthTask. However, the attempt did not result in the background task successfully reading and writing the database. 

- Then from further researching online, we found a solution which uses a new database session for background tasks. In addition to creating a scoped session for the background task, we also had to create a new sublass of Celery Tasks - 'SqlAlchemyTask' which removes the session at the end of the task to ensure a closed connection. 

## Implementing Neurosynth Viewer