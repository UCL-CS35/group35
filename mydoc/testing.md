---
title: Testing
sidebar: mydoc_sidebar
permalink: /testing/
---

## Unit Tesing using pytest

We tested INcDb on 2 different kind of test cases. 

1. The first kind is using the client which act like the browser, to navigate INcDb. We check that given each URL, the expected layout is return by confirming the content of the layout contain the keywords (usually the title of the page) we specified.

2. We also tested the Python functions like `find_or_create_user` to verify that data is added correctly into the database.

The set of test cases can be found at <https://github.com/UCL-CS35/incdb-poc/tree/master/tests>

### Issues Faced

As we try to keep each set of test cases independent, we intialise the database for every set of test cases. However, the initialisation of Neurosynth dataset take up a considerable amount of time (at least 5 minutes). Thus, we did not implement detailed and complicated test cases.

## Loading Stress Test

We used Loadster to test how our live demo handle multiple concurrent users. The Loadster simulate traffic conditions to identify breaking point of the website. The image below show the response times when 25 virtual users were simulated. For the full test result, <a href="{{ "/loadster/Test 1.html" | prepend: site.baseurl }}">click here.</a>

<img style="max-width:100%" src="{{ "/loadster/response_times.png" | prepend: site.baseurl }}" />

It was not surprising that the brain image file (anatomical.nii.gz?.nii.gz) has the highest average response times due to its larger file size. The average response times were below 0.2s for basic pages like the home, movie and term pages proved that INcDb was able to load smooth and quickly. 

## User Acceptance Testing

### Testing Strategy

User Acceptance Testing (UAT) is the last testing carried out before the software goes live. The main purpose of UAT to validate the software against the business requirements. Hence, prioritizing critical business objectives.

In our case, the objectives are:

1. INcDb provide a __simple and easy way__ to browse brain images. 

2. INcDb allow Neuroscientists to __contribute__ their data.

3. INcDb __match the Terms__ with the brain activation identified from the brain images.


There are 3 things that we considered during our coding and testing process:

1. Focus Testing on Requirements

2. Design Systems for Testability

3. Consider Usability Testing

Based on all of above, our testing strategy is to ensure that the product (every version of it) fits our final design requirements. In the process, we tested for the INcDb's workability, functionality, and to run the app on live remote server hosted by Digital Ocean.

Here’s a table for our results of testing on app functionality:

<img style="max-width:100%" src="{{ "/images/testing/uat.png" | prepend: site.baseurl }}" />

We design our test by identifying the features to be tested, the features not to be tested, the test environment and the targeted tester.

#### Features to be tested

* Repository Browsing
 
* Registration, Sign In and Sign Out

* Create Collection and Upload Dataset

#### Features not to be tested

* Upload Processed Dataset

#### Test Environment

* We let the testers use the demo version of INcDb at <http://188.166.170.92/> using Google Chrome Version 50.0.2661.86 in Incognito mode. The website is reset after each test.

### Targeted Tester

* Computer Science Students - We chose CS students, who are experienced in web development, as they know what to expect during an app testings and they are able to find flaws and fault in our app quickly ­ in fact that’s one of the main purpose of testing so that the app can be improved.

* Neuroscientist - The choice is made because neuroscientist are the target users and are experienced in interacting with the brain images. Their opinions matter especially on whether INcDb provide a reliable way to contribute their data.

### Response Received

Overall, we received positive feedbacks that the demo version of INcDb are able to completed the features that is to be tested. However, we also receive feedback on the issues our testers faced and suggestion for improvements such as:

1. Capitalising the words on the navigation bar to improve the professionalism of the website

2. Font size for the body content is too small

3. Colour of the upload progress bar does not match the colour scheme of INcDb

4. A more detailed Disclaimer Policy should be available.

5. "Not sure where to start?" on the home page is not prominent.

6. The upload process take a long time. 

### Conclusion

The feedback on the design of INcDb was useful to further polish our website to make it ready for the use by public. The suggestion for a more detailed Disclaimer Policy will be further discussed with our client and necessary changes will be made once he draft the new policy. However, the complaint on the long duration taken during the upload process cannot be resolved on our side. As the dataset are usually more than a gigabyte at least, the upload process will take a while even if the user has good connection speed. Beside having a progress bar to update the user on the progress of the uploading process, we will also look into including messages during the uploading process to remind the users to be patient with the uploading.

The User Acceptance Testing, which has real users to test the application, gave us an insight of how the users use the application and help us identify issues they faced and prepare the application to be used by the general public.

