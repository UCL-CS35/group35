---
title: Use Cases
keywords:
summary: "Use Cases developed for the development of INcDb."
sidebar: mydoc_sidebar
permalink: /use-cases/
---

We have written a list of use cases for our project. This list is subject to change during the development process.

<table>
  <thead>
    <tr>
      <th width="5%">ID</th>
      <th>Use Case</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Register an Account</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Login</td>
    </tr>
    <tr>
      <td>3</td>
      <td>View Movie</td>
    </tr>
    <tr>
      <td>4</td>
      <td>View Term for a specific Movie</td>
    </tr>
    <tr>
      <td>5</td>
      <td>View Term for all Movies</td>
    </tr>
    <tr>
      <td>6</td>
      <td>View Component</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Upload Raw Dataset</td>
    </tr>
    <tr>
      <td>8</td>
      <td>View Uploaded Raw Dataset Informationi</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Edit Uploaded Raw Dataset Information</td>
    </tr>
  </tbody>
</table>


<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>1: Register an Account</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, User, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>Actor not logged in, does not have an account</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The Visitor requests to create a new User account.<br>
        2. The Server responds with an application form, which includes fields for e-mail address and password.<br>
        3. The Visitor enters in their details and submits it to the Server.<br>
        4. The Server creates the new User account, and marks it to disabled. The User is emailed instructions on how to activate their account.<br>
        5. The Visitor receives the e-mail instructions, and follows the instructions to activate their account.<br>
        6. The Server marks the account as enabled, and redirects the Visitor to the "Login" page.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>New account registered, logged in, return to "My Collections" page</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>
        1. Failed to register new account, error message(s) shown on same page<br>
        A) Duplicate email.<br>
        B) Field(s) left blank.<br>
        2. The User does not follow through on the account activation; the account is automatically deleted after a period of inactivity.
      </td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>2: Login</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, User, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>Actor not logged in, owns an account</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. A Visitor goes to the "Login" page.<br>
        2. The Visitor enters in an email and password, and submits the form to the Server.<br>
        3. The Server checks their email and password against the list of existing user accounts, and verifies that the account exists.<br>
        4. The Server updates the Visitor’s session to indicate that they are an authorised User.<br>
        5. The Visitor becomes a User, and is redirected to "My Collections" page.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>Actor logged in, return to "My Collections" page</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>
        Invalid Login, error message shown on same page "Invalid Login, please login using registered email address and password, or register" and prevented from continuing.
      </td>
    </tr>
  </tbody>
</table>
      
<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>3: View Movie</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The Visitor requests a Movie from the list of Movies on "Movies" page.<br>
        2. The Server connects to the database and list the information (averaged brain images, list of Terms associated, list of Components) about the selected Movie
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>The database cannot be accessed; an error message is displayed</td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>4: View Term for a specific Movie</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The Visitor requests a Term from the list of Terms on "Movie" page.<br>
        2. The Server connects to the database and list the information (averaged brain images, list of Movies associated, list of Components) about the selected Term
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>The database cannot be accessed; an error message is displayed</td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>5: View Term for all Movies</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The Visitor requests a "Terms" page.<br>
        2. The Server connects to the database and list all available Terms.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>None</td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>6: View Component</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>Visitor, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. View Movie.<br>
        2. From list of Components under "Components" tab, select a Component.<br>
        OR<br>
        1. View Term (either for specific Movie or all Movies).<br>
        2. From list of Components under "Components" tab, select a Component.<br>
        <br>
        3.The Server connects to the database and list the information (averaged brain images, list of Terms associated) about the selected Component.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>None</td>
    </tr>
  </tbody>
</table>


<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>7: Upload Raw Dataset</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>User, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>User must be logged In</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The User attaches a file to the Dataset, by uploading a file to the Server.<br>
        2. The Server save this file to a temporary storage.<br>
        3. The User enter additional information for the Dataset.<br>
        4. Once, the User is finished, the file is uploaded and the temporary storage is deleted.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>New Dataset uploaded, pending analysis</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>
        1. The uploading process is disconnected.<br>
        2. File is not uploaded.<br>
        3. The User is redirect to the "Contribute" page.
    </td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>8: View Uploaded Raw Dataset Information</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>User, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>Logged In, Uploaded Dataset previously</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The Visitor requests a "Dataset" page.<br>
        2. The Server connects to the database and list information about the Dataset.
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>None</td>
    </tr>
  </tbody>
</table>

<table>
  <tbody>
    <tr>
      <th width="20%">Use Case</th>
      <td>9: Edit Uploaded Raw Dataset Information</td>
    </tr>
    <tr>
      <th>Primary Actors</th>
      <td>User, Server</td>
    </tr>
    <tr>
      <th>Secondary Actors</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Preconditions</th>
      <td>Logged In, Uploaded Dataset previously</td>
    </tr>
    <tr>
      <th>Main Flow</th>
      <td>
        1. The User requests the "Edit Dataset" page<br>
        2. The Server presents the "Edit Dataset" page, which contains all the fields on the dataset<br>
        3. The User changes one or more fields<br>
        4. The User submits the page back to the server<br>
        5. The Server changes the fields of the current Dataset to the value provided by the User<br>
        6. The User is redirected to the "Dataset" page
      </td>
    </tr>
    <tr>
      <th>Post Conditions</th>
      <td>None</td>
    </tr>
    <tr>
      <th>Alternative Flows</th>
      <td>
        1. The User does not have the permissions to edit the Dataset and an error message is displayed.<br>
        2. The database cannot be accessed; an error message is displayed.
      </td>
    </tr>
  </tbody>
</table>