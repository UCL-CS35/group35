---
title: Requirements
summary: "Project Requirements idenitfy for INcDb."
sidebar: mydoc_sidebar
permalink: /requirements/
---

We gather the project requirements through our discussions with our client, Dr Skipper and analysing similar project like NeuroVault and Neurosynth.

As individuals who don't have any knowledge on neuroscience, we also used ourselves as the target users and identify requirements that will be important to non-technical users like us.

The following list of requirements had been identified by the group and approved by our client, Dr. Skipper. Requirements are described using 'MoSCoW' approach, Must Have, Should Have, Could Have and Won't Have. The requirements are also label as Functional (what the system should do) and Non-Functional (how the system is supposed to) requirements.

## Final Requirements

* The client agree that Requirements No. 9 and No. 43 are not necessary and hence exlcuded from the final requirements.

* With the client's approval, 
	 
  * Requirements No. 48 and 49 are implemented with a web interface instead of command line.

  * Requirements No. 37 are implemented by disabling user to delete their datasets when the Processed Dataset is uploaded instead of the 24 hours period.

<table class="table">
	<thead>
	  <tr>
	    <th style="width:2%;">ID</th>
	    <th>Category</th>
	    <th>Requirement</th>
	    <th>Functional?</th>
	    <th>Priority</th>
	    <th>Users</th>
	  </tr>
	</thead>
	<tbody>
	  <tr>
	    <td>1</td>
	    <td>Availability</td>
	    <td>The Repository shall be available at all time.</td>
	    <td>Non-functional</td>
	    <td>Should</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>2</td>
	    <td>Performance</td>
	    <td>The Repository shall be able to support 10 concurrent Users at anytime.</td>
	    <td>Non-functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>3</td>
	    <td>User Interface</td>
	    <td>The Repository shall use a web browser as its interface.</td>
	    <td>Non-functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>4</td>
	    <td>User Interface</td>
	    <td>The Repository shall have a responsive layout.</td>
	    <td>Non-functional</td>
	    <td>Could</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>5</td>
	    <td>Platform Constraints</td>
	    <td>The Repository shall support major modern browsers like Google Chrome, Firefox and Internet Explorer.</td>
	    <td>Non-functional</td>
	    <td>Should</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>6</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of latest 10 Movies withProcessed Dataset.
	    <br><a href="http://188.166.170.92/">http://188.166.170.92/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>7</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a search box for Movies with Processed Dataset.
	    <br><a href="http://188.166.170.92/">http://188.166.170.92/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>8</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a paginated list of all Movies with Processed Dataset.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr style="text-decoration:line-through;">
	    <td>9</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis average image of all brain images for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>10 </td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a 3-tabs layout for Terms (default), Components and Details.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>11</td>
	    <td>Repository Browsing</td>
	    <td>The Repository  shall display a list of highly associated Terms for a specific Movie.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>12</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Components for a specific Movie.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>13 </td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis average image of all Components for a specific Term for a specific Movie.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>14</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Components for a specific Term for a specific Movie.
	    <br><a href="http://188.166.170.92/movies">http://188.166.170.92/movies</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>15</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Movies associated with specific Terms.
	    <br><a href="http://188.166.170.92/terms/pain/">http://188.166.170.92/terms/pain/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>16</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display an option to view selected Term for all Movies.
	    <br><a href="http://188.166.170.92/terms/pain/">http://188.166.170.92/terms/pain/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>17</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis image of specific Component for a specific Movie.
	    <br><a href="http://188.166.170.92/component/###/">http://188.166.170.92/component/###/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>18</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of Terms available for a specific Component for a specific Movie.
	    <br><a href="http://188.166.170.92/component/###/">http://188.166.170.92/component/###/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>19</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Terms matched to any Component in the Database.
	    <br><a href="http://188.166.170.92/terms/">http://188.166.170.92/terms/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>20</td>
	    <td>Repository Browsing</td>
	    <td>The repository shall display the average image of all Components for a specific Term for all Movies.
	    <br><a href="http://188.166.170.92/terms/pain/">http://188.166.170.92/terms/pain/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>21</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a questions and answers layout explaining How to use, Terms and Components.
	    <br><a href="http://188.166.170.92/guide">http://188.166.170.92/guide</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>22</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to upload their Raw Dataset to the server.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>23</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to upload multiple files.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>24</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to the describe the files to be uploaded.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>25</td>
	    <td>Data Submission &amp; Reliability</td>
	    <td>The Repository shall ensure that the upload process is reliable with more than 95% success rate.</td>
	    <td>Non-functional</td>
	    <td>Could</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>26</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display an FAQ for questions that might arise with regard to collecting the Raw Dataset.
	    <br><a href="http://188.166.170.92/faq">http://188.166.170.92/faq</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>27</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Essentials information of the Raw Dataset.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must </td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>28</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Participants information of the Raw Dataset.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>29</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Design information of the Raw Dataset.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>30</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Acquisition information of the Raw Dataset.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>31</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Movie information of the Raw Dataset.
	    <br><a href="http://188.166.170.92/contribute/new">http://188.166.170.92/contribute/new</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>32</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display an animated progress bar and percentage during the uploading process.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>33</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a warning dialog when User try to close the page when the uploading process is ongoing.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>34</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a list of User’s uploaded Raw Datasets.
	    <br><a href="http://188.166.170.92/user/collections">http://188.166.170.92/user/collections</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>35</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display information of the Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>36 </td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a disclaimer policy on Dataset collected.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	    </tr>
	  <tr>
	    <td>37</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to delete his/her uploaded Datasets <span style="text-decoration:line-through">during a grace period of 24 hours</span> before the admin upload a Processed Dataset for the collection.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>38</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a warning dialog when User try to delete a Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>39</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to register an account with email, initial, first and last name.
	    <br><a href="http://188.166.170.92/user/register">http://188.166.170.92/user/register</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>40</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to login and logout.
	    <br><a href="http://188.166.170.92/user/sign-in">http://188.166.170.92/user/sign-in</a>
	    <br><a href="http://188.166.170.92/user/sign-out">http://188.166.170.92/user/sign-out</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>41</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to reset password.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>42</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to change password.
	    <br><a href="http://188.166.170.92/user/change-password">http://188.166.170.92/user/change-password</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>44</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to edit initial.
	    <br><a href="http://188.166.170.92/user/account">http://188.166.170.92/user/account</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>45</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to edit first and last name.
	    <br><a href="http://188.166.170.92/user/account">http://188.166.170.92/user/account</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>46</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to add affiliation.
	    <br><a href="http://188.166.170.92/user/account">http://188.166.170.92/user/account</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>47</td>
	    <td>User Management &amp; Security</td>
	    <td>The Repository shall only allow user to edit their personal information.
	    <br><a href="http://188.166.170.92/user/account">http://188.166.170.92/user/account</a>
	    </td>
	    <td>Non-Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>              
	  <tr>
	    <td>48</td>
	    <td>Admin</td>
	    <td>The Repository shall allow administrator to download Raw Datasetset <span style="text-decoration:line-through">using command line</span> via web interface.
	    <br><a href="http://188.166.170.92/admin/">http://188.166.170.92/admin/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>Admin</td>
	    </tr>
	  <tr>
	    <td>49</td>
	    <td>Admin</td>
	    <td>The Repository shall allow administrator to upload Processed Dataset <span style="text-decoration:line-through">using command line</span> via web interface.
	    <br><a href="http://188.166.170.92/admin/">http://188.166.170.92/admin/</a>
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>Admin</td>
	  </tr>
	</tbody>
</table>

## Initial Requirements (from COMP204P)

<table class="table">
	<thead>
	  <tr>
	    <th style="width:2%;">ID</th>
	    <th>Category</th>
	    <th>Requirement</th>
	    <th width="12%">Functional?</th>
	    <th>Priority</th>
	    <th>Users</th>
	  </tr>
	</thead>
	<tbody>
	  <tr>
	    <td>1</td>
	    <td>Availability</td>
	    <td>The Repository shall be available at all time.</td>
	    <td>Non-functional</td>
	    <td>Should</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>2</td>
	    <td>Performance</td>
	    <td>The Repository shall be able to support 10 concurrent Users at anytime.</td>
	    <td>Non-functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>3</td>
	    <td>User Interface</td>
	    <td>The Repository shall use a web browser as its interface.</td>
	    <td>Non-functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>4</td>
	    <td>User Interface</td>
	    <td>The Repository shall have a responsive layout.</td>
	    <td>Non-functional</td>
	    <td>Could</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>5</td>
	    <td>Platform Constraints</td>
	    <td>The Repository shall support major modern browsers like Google Chrome, Firefox and Internet Explorer.</td>
	    <td>Non-functional</td>
	    <td>Should</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>6</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of latest 10 Movies withProcessed Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>7</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a search box for Movies with Processed Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>8</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a paginated list of all Movies with Processed Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>9</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis average image of all brain images for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>10 </td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a 3-tabs layout for Terms (default), Components and Details.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>11</td>
	    <td>Repository Browsing</td>
	    <td>The Repository  shall display a list of highly associated Terms for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>12</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Components for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>13 </td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis average image of all Components for a specific Term for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>14</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Components for a specific Term for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>15</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Movies associated with specific Terms.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>16</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display an option to view selected Term for all Movies.
	    </td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>17</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display the 3-axis image of specific Component for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>18</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of Terms available for a specific Component for a specific Movie.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>19</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a list of all Terms matched to any Component in the Database.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>20</td>
	    <td>Repository Browsing</td>
	    <td>The repository shall display the average image of all Components for a specific Term for all Movies.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>21</td>
	    <td>Repository Browsing</td>
	    <td>The Repository shall display a questions and answers layout explaining How to use, Terms and Components.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>22</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to upload their Raw Dataset to the server.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>23</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to upload multiple files.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>24</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to the describe the files to be uploaded.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>25</td>
	    <td>Data Submission &amp; Reliability</td>
	    <td>The Repository shall ensure that the upload process is reliable with more than 95% success rate.</td>
	    <td>Non-functional</td>
	    <td>Could</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>26</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display an FAQ for questions that might arise with regard to collecting the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>27</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Essentials information of the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must </td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>28</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Participants information of the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>29</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Design information of the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>30</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Acquisition information of the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>31</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to input Movie information of the Raw Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>32</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display an animated progress bar and percentage during the uploading process.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>33</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a warning dialog when User try to close the page when the uploading process is ongoing.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>34</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a list of User’s uploaded Raw Datasets.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>35</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display information of the Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>36 </td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a disclaimer policy on Dataset collected.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	    </tr>
	  <tr>
	    <td>37</td>
	    <td>Data Submission</td>
	    <td>The Repository shall allow User to delete his/her uploaded Datasets during a grace period of 24 hours.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>38</td>
	    <td>Data Submission</td>
	    <td>The Repository shall display a warning dialog when User try to delete a Dataset.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>39</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to register an account with email, initial, first and last name.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>40</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to login and logout.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>41</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to reset password.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>42</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to change password.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>43</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to delete account.</td>
	    <td>Functional</td>
	    <td>Should</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>44</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to edit initial.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>45</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to edit first and last name.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>46</td>
	    <td>User Management</td>
	    <td>The Repository shall allow User to add affiliation.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>
	  <tr>
	    <td>47</td>
	    <td>User Management &amp; Security</td>
	    <td>The Repository shall only allow user to edit their personal information.</td>
	    <td>Non-Functional</td>
	    <td>Must</td>
	    <td>All</td>
	  </tr>              
	  <tr>
	    <td>48</td>
	    <td>Admin</td>
	    <td>The Repository shall allow administrator to download Raw Datasetset using command line.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>Admin</td>
	    </tr>
	  <tr>
	    <td>49</td>
	    <td>Admin</td>
	    <td>The Repository shall allow administrator to upload Processed Dataset using command line.</td>
	    <td>Functional</td>
	    <td>Must</td>
	    <td>Admin</td>
	  </tr>
	</tbody>
</table>