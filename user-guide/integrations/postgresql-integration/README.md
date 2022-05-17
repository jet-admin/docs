---
description: Connecting a database to Jet Admin.
---

# Database Integration

To connect a database with **Jet Admin**, choose a database from the list of available integrations:

![](<../../../.gitbook/assets/image (816).png>)

Then choose a set up method. Use [instant cloud](instant-cloud.md) installation to connect Jet Admin with your public database directly (localhost not valid). If you care about your sensitive data we provide [Jet Bridge](../../../jet-bridge-deployment/jet-admin/) installation. It will connect to your database and link **Jet Admin** with your project. It will work even with your application on **localhost**. Use [Docker](docker-installation.md) or [Python](python-app-installation.md) Installation to deploy Jet Bridge.

![](<../../../.gitbook/assets/image (817).png>)

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

{% content-ref url="../../../jet-bridge-deployment/database-heroku-deployment.md" %}
[database-heroku-deployment.md](../../../jet-bridge-deployment/database-heroku-deployment.md)
{% endcontent-ref %}

### Connect through SSH

You can use SHH to **safely integrate** with databases in Jet. Simply enable the toggle here and paste the credentials:

![](../../../.gitbook/assets/dxjctyj.png)

### Make a SQL queries

Using Database integration you can make simple or [SQL queries](../../data/make-a-sql-query.md) to your database:

![](../../../.gitbook/assets/testgif13.gif)

{% content-ref url="../../data/make-a-sql-query.md" %}
[make-a-sql-query.md](../../data/make-a-sql-query.md)
{% endcontent-ref %}



