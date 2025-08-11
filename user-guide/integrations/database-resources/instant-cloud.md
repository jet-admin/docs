---
description: Step-by-step guide to Cloud Installation.
---

# Instant Installation

The quickest way to integrate database (**localhost** not valid, use [**Docker**](docker-installation.md) or [**Python**](python-app-installation.md) integration instead). We encrypt all data and credentials that go through our servers using an HTTPS connection.

You'll need to fill out the following form:

![](<../../../.gitbook/assets/image (818).png>)

| Name               | Description                                                                                                                                                                                           |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Host               | The IP address or hostname (db.example.com) of where your database instance resides. Note, `localhost` and **`127.0.0.1` are not valid!** Make sure it is accessible from these IPs: `95.179.253.121` |
| User               | Username for this database                                                                                                                                                                            |
| Password           | Password for this database                                                                                                                                                                            |
| Database Name      | The name of the database you would like to interact with.                                                                                                                                             |
| Database Port      | Port to connect to. By default PostgreSQL: 5432                                                                                                                                                       |
| PostgreSQL Schema  | Your database schema (`optional`)                                                                                                                                                                     |
| Extra Parameters   | Extra parameters, ex. charset=utf8 (`optional`)                                                                                                                                                       |

### Make a SQL queries

Using Database integration you can make simple or [SQL queries](../../data/make-a-sql-query.md) to your database:

{% @arcade/embed flowId="Fg2gqwiVIpsgGl7YNdlq" url="https://app.arcade.software/share/Fg2gqwiVIpsgGl7YNdlq" %}

Here is a [step-by-step guide](../../../jet-bridge-deployment/database-heroku-deployment.md) to deploying the database to Heroku and finding your credentials.

{% content-ref url="../../../jet-bridge-deployment/database-heroku-deployment.md" %}
[database-heroku-deployment.md](../../../jet-bridge-deployment/database-heroku-deployment.md)
{% endcontent-ref %}
