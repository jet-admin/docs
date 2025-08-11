---
description: Connect Jet Admin to any REST API.
---

# Rest API

In addition to ready-to-use integrations, Jet Admin allows you to use REST API to connect to any tool you need to integrate into your workflow.&#x20;

{% embed url="https://youtu.be/MlNuOS2sffQ" %}

To connect a REST API or another resource, first select Add Resource from the project menu to open the resource selection pane:

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

You can also implement your own custom API using API Builder. For example, you can set up GET or POST requests to retrieve or update data based on your application's needs.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% content-ref url="../../data/make-an-http-request.md" %}
[make-an-http-request.md](../../data/make-an-http-request.md)
{% endcontent-ref %}

### Connect custom API resource

Let's start with implementing **Rest API**, select it from the list of available resources, and specify the general information that will use for all API requests for this resource:&#x20;

* **Resource name** – unique name that indicates API resource in Jet Admin.
* **Base URL** – URL that will use for all requests for this resource (if you want to use different URL, create different resources for each URL).
* **Authentication** –  used to authenticate requests: [Bearer token](bearer-token.md), [Basic Auth](basic-authentication.md), [OAuth 2.0](oauth-2.0.md).

![](<../../../.gitbook/assets/image (617).png>)

Once you have connected a REST API, you will need to configure the requests in the Data Editor. For more information, please look at the [Data Editor documentation here:](https://docs.jetadmin.io/user-guide/data/make-an-http-request)

{% content-ref url="../../data/make-an-http-request.md" %}
[make-an-http-request.md](../../data/make-an-http-request.md)
{% endcontent-ref %}

