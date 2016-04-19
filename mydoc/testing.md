---
title: Testing
last_updated: March 20, 2016
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