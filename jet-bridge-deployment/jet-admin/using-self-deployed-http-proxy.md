---
description: In this section you will learn how to use self-deployed HTTP proxy
---

# Using self-deployed HTTP proxy

By default, all queries for **HTTP-based resources** (**Custom Rest API, 3rd party integrations**) are sent by **Jet Admin** through our **Jet Bridge** proxy endpoint at [https://api.jetadmin.io/api/proxy\_request/](https://api.jetadmin.io/api/proxy\_request/) for convenience. Requests data going through our servers are never being recorded, but if you don't want data to go through **Jet Admin** servers you can use a self-hosted **HTTP Proxy** on your side as part of an open-source **Jet Bridge** application.

## Using self-deployed HTTP proxy

Follow the instructions after you have created the **Jet Admin** **Rest API** resource:

#### 1. Install Jet Bridge

Use the following guides to install the **Jet Bridge** application as a standalone **Python application** or **Docker container.**

{% content-ref url="../../user-guide/integrations/postgresql-integration/python-app-installation.md" %}
[python-app-installation.md](../../user-guide/integrations/postgresql-integration/python-app-installation.md)
{% endcontent-ref %}

{% content-ref url="../../user-guide/integrations/postgresql-integration/docker-installation.md" %}
[docker-installation.md](../../user-guide/integrations/postgresql-integration/docker-installation.md)
{% endcontent-ref %}

{% hint style="info" %}
You can skip a database configuration part and use **Jet Bridge** just for proxying **HTTP requests**. For such cases use **none** for the **DATABASE\_ENGINE** configuration parameter.
{% endhint %}

After installation specify the following parameter if you don't want to place **Jet Bridge** behind your web server and set CORS headers on your own:\
**ALLOW\_ORIGIN** = \<Jet Admin hostname> (https://app.jetadmin.io or your custom domain)

Check the link below to learn how to specify **Jet Bridge** configuration:

{% content-ref url="configuration.md" %}
[configuration.md](configuration.md)
{% endcontent-ref %}

#### 2. Run Jet Bridge

**3. Update resource to use custom HTTP proxy**

In resource settings click the **Edit Settings** button and set **Custom HTTP proxy** to your **Jet Bridge** proxy request URL:\
<**JET\_BRIDGE\_HOST>/api/proxy\_request/**

For example for Jet Bridge running on localhost and port 8888 this will be: \
[http://localhost:8888/api/proxy\_request/](http://localhost:8888/api/proxy\_request/)

![](<../../.gitbook/assets/image (522).png>)

#### 4. You are done!

Now all HTTP queries for this resource will be sent through your server.
