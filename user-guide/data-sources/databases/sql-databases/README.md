---
description: Connect your PostgreSQL, MySQL, SQL Server and MariaDB databases to Jet apps.
icon: database
---

# SQL Databases

## Connecting database as a resource

We support direct connection to various databases, as well as connections to 3rd party database services.

To connect a database with **Jet Admin**, choose a database from the list of available integrations:

<figure><img src="../../../../.gitbook/assets/image (1022).png" alt=""><figcaption></figcaption></figure>

### SQL databases

* PostgreSQL
* MySQL
* Microsoft SQL
* MariaDB
* SQLite
* Oracle
* AlloyDB

### Other data sources

* [Supabase](../supabase.md)
* [Airtable](../../spreadsheets-and-collaborative-databases/airtable.md)
* [Google Sheets](../../../../classic-app-builder/videos/connecting-data-sources/google-sheet.md)
* [Firebase](../firebase-firestore/firestore.md)
* [Xano](../xano.md)
* BigQuery
* [Snowflake](../snowflake.md)
* [SmartSuite](../../business-apps/smartsuite.md)
* Microsoft SQL
* Amazon Redshift

After choosing a database, you'll need to choose set up method.

{% hint style="info" %}
Set up methods may vary depending on database you choose.
{% endhint %}

Use [instant cloud](instant-cloud.md) installation to connect Jet Admin with your public database directly (you won't be able to connect to localhost databases).

We also provide [Jet Bridge](../../../../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/jet-admin/) to manage data in case you want to add an extra layer of security for your sensitive data. It will connect to your database and link **Jet Admin** with your project. It will work even with your application on **localhost**. Use [Docker](docker-installation.md) or [Python](python-app-installation.md) Installation to deploy Jet Bridge.

![](<../../../../.gitbook/assets/image (817).png>)

{% content-ref url="instant-cloud.md" %}
[instant-cloud.md](instant-cloud.md)
{% endcontent-ref %}

{% content-ref url="docker-installation.md" %}
[docker-installation.md](docker-installation.md)
{% endcontent-ref %}

{% content-ref url="python-app-installation.md" %}
[python-app-installation.md](python-app-installation.md)
{% endcontent-ref %}

### Deploy database to Heroku

An example of database deployment on Heroku and further Instant method integration.

{% content-ref url="../../../../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/database-heroku-deployment.md" %}
[database-heroku-deployment.md](../../../../jet-bridge-deployment/cloud-jet-bridge-and-on-premises/database-heroku-deployment.md)
{% endcontent-ref %}

### Connect through SSH

You can use SHH to **safely integrate** with databases in Jet Admin, if databases support it. Simply enable the toggle here and paste the credentials:

![](../../../../.gitbook/assets/dxjctyj.png)

### Make an SQL queries

Using Database integration you can make simple or [SQL queries](../../../sql-queries-and-api-requests/make-a-sql-query.md) to your database to select the data and use it as virtual tables:

{% @arcade/embed url="https://app.arcade.software/share/Fg2gqwiVIpsgGl7YNdlq" flowId="Fg2gqwiVIpsgGl7YNdlq" %}

{% content-ref url="../../../sql-queries-and-api-requests/make-a-sql-query.md" %}
[make-a-sql-query.md](../../../sql-queries-and-api-requests/make-a-sql-query.md)
{% endcontent-ref %}
