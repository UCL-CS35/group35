---
layout: page
title: Requirements
permalink: /requirements/
---

We gather the project requirements through our discussions with our client, Dr Skipper and analysing similar project like NeuroVault and Neurosynth.

As individuals who don't have any knowledge on neuroscience, we also used ourselves as the target users and identify requirements that will be important to non-technical users like us.

The following list of requirements had been identified by the group and approved by our client, Dr. Skipper. Requirements are described using 'MoSCoW' approach, Must Have, Should Have, Could Have and Won't Have. The requirements are also label as Functional (what the system should do) and Non-Functional (how the system is supposed to) requirements.

<hr>

**Final Requirements identified for the Final Proof of Concept**

* The Repository is live at <a href="http://188.166.170.92/">http://188.166.170.92/</a>.

* The client agree that Requirements No. 9 - "The Repository shall display the 3-axis average image of all brain images for a specific Movie." is not necessary and hence exlcuded from the final requirements.

* With the client's approval, Requirements No. 48 and 49 are implemented with a web interface instead of command line.

* Requirements No. 37, 41, 43 (pending discussion with client)

<table>
	<thead>
	  <tr>
	    <th>ID</th>
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

<hr>

**Initial Requirements (from COMP204P)**

<table>
	<thead>
	  <tr>
	    <th>ID</th>
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

<hr>

### Use Cases

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

<hr>

### Glossary

We build a Glossary of Terms to define vocublary for the project so that the group and the client uses the same definition during the discussion of the project.

<table>
  <thead>
    <tr>
      <th>Term</th>
      <th>Definition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Term</td>
      <td>The keyword that describe the brain activation.</td>
    </tr>
    <tr>
      <td>Component</td>
      <td>An analysed image that contain the x-y-z axis of a dataset.</td>
    </tr>
    <tr>
      <td>Repository or INcDb</td>
      <td>The web application that will be publically available.</td>
    </tr>
    <tr>
      <td>Processed Dataset</td>
      <td>The set of files that are produced after our client has run the analysis process on the Raw Dataset.</td>
    </tr>
    <tr>
      <td>Raw Dataset</td>
      <td>The set of brain images collected by researcher when someone watch a movie.</td>
    </tr>
  </tbody>
</table>