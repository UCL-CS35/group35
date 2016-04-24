---
title: Testing Strategy
tags: 
keywords:
sidebar: mydoc_sidebar
permalink: /research/testing-strategy/
---

This page details the testing strategies that we will be adpoting to ensure the our PoC will be working properly.

## Unit Testing
We had conducted research on Flask-Testing and pytest for our unit testing strategy. Flask-Testing is a Flask extension that provides us with a set of test utilities tools to conduct unit test on our codes. Pytest is a mature features-rich testing tool that can be used on any Python programs. We decided to use pytest because it has comprehensive documentation and there are plenty of troubleshoot resources available online.

We need to add `pytest` and `pytest-flask` to our requirements.txt and then run `pip install -r requirements.txt`. Test cases are written in individual Python file located at `/app-name/tests/`. A shell script was written to run the test cases.

## Acceptance Testing
Acceptance tests are used to verify that a story (requirement) is complete. The tests are described in plain English and ensures the software, as a whole, is feature complete.

For acceptance testing, we will be using Lettuce. The test cases will be written in Gherkin Syntax. We need to write 2 files, Feature and Step. Feature files are written in plain English, and specify the area of the application that the tests cover. It include 3 key areas, Feature, Background and Scenario. Feature is a descripion of the feature to be tested. Background is executed before Scenario and setup the necessary conditions before running the test. Scenario define the test. Step file match each line in the Scenario to the Python code through Regular Expressions.

## Web Testing
Besides conducting unit testing and acceptance, we will be conducting web testing using Selenium. It a toolkit that allows us to run our web application on a selected browser and conduct test case on it. We will be using Selenium IDE which record the sequence of user's actions and clicks in each test case. We will then run all the suite of all the test cases to start the automated testing process.

## Unit Testing on Prototype
For our Term 1 prototype, we ran a few test cases checking the functionality of user management. The test cases include tesing if user can change password, edit their title, and first name and last name. The source code for the test cases are located at <https://github.com/UCL-CS35/incdb-user/blob/master/tests/test_user_management.py>.

To run the test, at the project folder, type `./runtests.sh`. The image below is the result of running the test cases.

![Test Result]({{ "/images/research/testresult.png" | prepend: site.baseurl }})
