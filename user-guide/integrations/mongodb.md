---
description: >-
  MongoDB is a cross-platform document-oriented database platform. Classified as
  a NoSQL database product, MongoDB uses JSON-like format to store documents
  with optional schemas.
---

# MongoDB

Before Connection MongoDB with Jetadmin, you need to have a "Connection String" and the "Database Name".

## Get MongoDB's Connection String <a href="#connect-airtable-to-jetadmin" id="connect-airtable-to-jetadmin"></a>

1. Go to the [MongoDB Atlas web interface](https://cloud.mongodb.com/) ,and on the left menu, Click "Clusters"
2. Click on the "Connect" button next to the needed cluster's name
3. Choose "Compass"
4. Copy the provided Connection String
5. Click "Done"

<div align="left" data-full-width="false">

<figure><img src="../../.gitbook/assets/image (963).png" alt=""><figcaption></figcaption></figure>

</div>

In the connection string, replace **\<db\_password>** with the password for the **Current User** you were provided before when registering a new user in MongoDB.

{% hint style="info" %}
If you lost your password, you need to create a new one.
{% endhint %}

#### To create a new password, follow the steps below:

1. On the left menu, Click on "Database Access" link in the sidebar under the "Security" section
2. Under the Database users tab, find the needed user and click the "Edit" button next to it
3. In the next screen, Click on "Edit Password"
4. Type a new password, Copy, and **save it** in a safe place.

<div align="left">

<figure><img src="../../.gitbook/assets/image (964).png" alt=""><figcaption></figcaption></figure>

</div>

## Get the Database Name <a href="#connect-airtable-to-jetadmin" id="connect-airtable-to-jetadmin"></a>

1. Go to the needed Cluster
2. Under the "Collections" tab, click to choose the needed Database
3. Copy the Database name.

<div align="left">

<figure><img src="../../.gitbook/assets/image (965).png" alt=""><figcaption></figcaption></figure>

</div>

## Connect MongoDB to Jetadmin <a href="#connect-airtable-to-jetadmin" id="connect-airtable-to-jetadmin"></a>

1. On Jetadmin's builder side, click 'Add Resource' from the data section on the left-side menu
2. Choose MongoDB
3. Choose "Instant Connection" as a setup method
4. Type a unique name for the new MongoDB data source
5. Choose the suitable region which is closer to your location and has less delay
6. Paste the "Connection string" that was prepared before
7. Paste the "Database Name"
8. Click the 'Choose tables' button
9. Select/unselect the needed tables
10. Click the 'Add Resource' button.

<div align="left" data-full-width="false">

<figure><img src="../../.gitbook/assets/image (966).png" alt=""><figcaption></figcaption></figure>

</div>



\
