---
description: Step-by-step guide to deploying a PostgreSQL database on Heroku.
---

# ⛺️ Database Heroku deployment

Once you have created the project, connected the resource, and selected the [Instant Cloud](../user-guide/integrations/database-resources/instant-cloud.md) deployment method you need to deploy your database on hosting.

In this step-by-step guide, we'll take a closer look at the complete database deployment process on [Heroku](https://www.heroku.com/).

### 1. Sign up for Heroku

To deploy your database you need to [sign up](https://signup.heroku.com/) a free Heroku account. You need to fill in the data and just click on **Create a free account**.

![](<../.gitbook/assets/image (383).png>)

### 2. Create a new app

Once you have completed the registration process, you will see this page. Just click on **Create new app**.&#x20;

![](<../.gitbook/assets/image (384).png>)

The next step is to specify the application name. Keep in mind that you can't use spaces and symbols. You also have to choose a region.

![](<../.gitbook/assets/image (385).png>)

### 3. Configure your application

Go to the Resources menu. Just search for **Postgres** in the add-ons and select it.

![](<../.gitbook/assets/image (386).png>)

Then you need to choose a plan for the add-on. Depending on it you'll have different resources. For test purposes, we will pick **Hobby Dev - free**.

![](<../.gitbook/assets/image (387).png>)

### 4. Find the credentials

Now you have a working Postgres database. You need to find the credentials. Click on Heroku Postgres to find the data you need.

![](<../.gitbook/assets/image (388).png>)

Go to the settings and click View Credentials.

![](<../.gitbook/assets/image (389).png>)

You need to enter these data in the fields required by the [Instant Cloud](../user-guide/integrations/database-resources/instant-cloud.md) deployment method.

![](<../.gitbook/assets/image (373).png>)

Congratulations! You've deployed your database on Heroku. Now you're ready to [integrate](../user-guide/integrations/) it into Jet Admin.
