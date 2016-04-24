---
title: Deployment
sidebar: mydoc_sidebar
permalink: /research/deployment/
toc: false
---

As our web application will be using the Python Flask Framework, the deployment server/service we will be using must support Python Flask applications. To deploy our web application, we could use a server provided by UCL or a cloud service.

1. If we do use a local server, there are several advantages. Firstly, we do not need to purchase subscriptions for the cloud services, and may have less restrictions.
2. Heroku is one of the cloud services which we found to support Python Flask web applications. It provides easy deployment methods such as simply pushing from a Git repository, then automatically compiles and run the application.
3. Similarly, Digital Ocean also supports Python Flask, with their main feature being speed, they supply cloud servers running with solid state drives, so data access would be faster. In addition, they give a choice of a magnitude of Linux distributions to be installed on the server.
4. Microsoft Azure is another cloud hosting platform which may be considered. One of its features is the access to a large number of APIs, connecting to other services is easier. It also supports "continuous integration", so pushes to GitHub can be automatically built, tested and deployed.

As our client does not have any prior knowledge of the deployment services available, he requested the group for a summary of the services. We researched on the three services, Heroku, Digtial Ocean and Microsoft Azure and comipled the information into the table below.

<table class="table table-striped table-bordered">
    <thead>
    <tr>
      <th>Heroku-Free</th>
      <th>Digital Ocean - 1TB Transfer</th>
      <th>Microsoft Azure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <ul>
          <li>Sleep after 30 minutes of inactivity</li>
          <li>Must sleep 6 hours in a 24 hour period</li>
          <li>Custom Domains</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>512MB Memory</li>
          <li>Single-core processor</li>
          <li>20GB SSD</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Shared Cores</li>
          <li>500MB RAM</li>
          <li>1GB Storage</li>
          <li>2GB SQL Database</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>At zero cost</li>
          <li>Great tools for deployment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Have control over virtual machine</li>
          <li>Well-designed tutorials to setup environment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Free student version</li>
          <li>Reliable provider</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>Not available at all times</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Require user to setup environment</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Confusing pricing model</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <a href="https://www.heroku.com/pricing">https://www.heroku.com/pricing</a>
      </td>
      <td>
        <a href="https://www.digitalocean.com/pricing/">https://www.digitalocean.com/pricing/</a>
      </td>
      <td>
        <a href="https://azure.microsoft.com/en-gb/pricing/">https://azure.microsoft.com/en-gb/pricing/</a>
      </td>
    </tr>
    <tr>
      <td>Free</td>
      <td>£3.32 ($5) per month</td>
      <td>£5.91 per month</td>
    </tr>
  </tbody>
</table>

We reach an agreement with our client to select Heroku. We choose Heroku because it offer a Free plan that will reduce the cost required during the development stage. As Heroku also provide a url for the web application deployed on the free plan, our client dose not need to purchase the domain name before INcDb is ready to go live. The restriction of 6 hours of downtime is not critical during the development stage too.