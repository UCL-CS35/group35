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
10. System manual

# Architectural Diagrams
Deployment Diagram
<object data="../images/diagrams/deployment.svg" width="100%" type="image/svg+xml">
</object>

Half Finished Class Diagram
<img src="../images/diagrams/class.svg" style="width:100%">


# User Guide v0.1

* Repository Browsing

* Data Submission

* User Management

* Administrative Privileges

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


