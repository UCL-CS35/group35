---
title: Development Plan
sidebar: mydoc_sidebar
permalink: /development/plan/
---

## Plan

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

## Iterations

### #1 - User Management 

The first iteration of INcDb is the prototype done for COMP204P in Term 1. The app used Flask-User to implement the user management feature. We used the Flask-User starter app as the base and modify the code to suit our the project requirements. We changed the details of the default account and added extra fields like 'Title' and 'Affiliation'. 

### #2 - Repository Browsing

**Neurosynth Dataset generation, Database design, Computation of correlation between Component and Terms, Repository Browsing**

The second iteration include adding the Neurosynth Dataset to the application, developing the database structure, implemeting the decoding function and basic repository browsing capability. This iteration include multiple features that are interconnected. The dataset and database was necessary for the decoding function to work and the repository browsing is included in this iteration to ensure that the database structure is well designed. 

Although we can use database query to check that the decoding function insert data to the database as designed, adding the repository browsing can help us improve the database design so that the query to retreive the necessary data will be kept simple.


### #3 - Data (Raw Dataset) Submission by User

With the user management implemented in Iteration #1, we added the ability to upload data for signed in user. During this iteration, we added a new table, `Collections`, to the database and a `uploads` folder to the application to store the Raw Dataset uploaded by the user. We also implemented a progress bar to inform user of the upload process. 

### #4 - Front-End Design

As the basic features of the application is mostly completed, we started to implement the front-end design based on the agreed mockup on the application during this iteration. We make changes to the original the mockup based on the feedback from our client and TA. The changes include capitalising the first letter to improve the professionalism of the site and increase the font-size of the body text to improve readability.

### #4 - Neurosynth Viewer

With the design in place, we started working on adding the Neurosynth Viewer to the application. The Neurosynth Viewer is a tool to display the brain images with sliders to interact with the images. We also added the merging function during this iteration. The merging function combines all the brain images (Component) of the Movie for a specific Term and display them using the Neurosynth Viewer.
 
### #5 - Moving decoding funtion to a background task

During this iteration, we move the decoding function to a backgroun task. As the decoding function compute the correlations between each Component uploaded and each Term in the database, it take a long time to complete. It is not feasible to get our Client to wait for both the uploading and the decoding. Hence, we used a background task to run the process and our Client can carry on managing the application after uploading the Processed Dataset.

### #6 - Unit Tests

The final iteration of INcDb include the testing the application using basic unit test cases. For details of the testing, please refer to the Testing page.