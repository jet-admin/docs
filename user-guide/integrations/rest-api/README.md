---
description: Connect Jet Admin to any REST API.
---

# Rest API

**Jet Admin** can help you make your tool make requests to any **Rest API** you need to integrate to your workflow. The integrations Jet provides are ready-to-use business APIs such as [Stripe](../stripe.md), [SendGrid](../sendgrid.md), [Zendesk](../zendesk.md), [Slack](../slack.md), etc. (To reduce the time to get your internal tool talking to a Rest API to the minimum, use the [Templates](broken-reference)). To have the  available APIs at hand, select Resources from the project menu to open the resource selection pane:

![](<../../../.gitbook/assets/image (821).png>)

You can also implement your own custom API using API Builder. For instance, you can set up a `GET` request to [display orders your customers made](../../../getting-started/part-2-intermediate/perform-api-requests.md) or a `POST` request to reset a password for a specific user. &#x20;

![](<../../../.gitbook/assets/image (822).png>)

{% content-ref url="../../data/make-an-http-request.md" %}
[make-an-http-request.md](../../data/make-an-http-request.md)
{% endcontent-ref %}

### Connect custom API resource

Let's start with implementing **Rest API**, select it from the list of available resources, and specify the general information that will use for all API requests for this resource:&#x20;

* **Resource name** – unique name that indicates API resource in Jet Admin.
* **Base URL** – URL that will use for all requests for this resource (if you want to use different URL, create different resources for each URL).
* **Authentication** –  used to authenticate requests: [Bearer token](bearer-token.md), [Basic Auth](basic-authentication.md), [OAuth 2.0](oauth-2.0.md).

![](<../../../.gitbook/assets/image (617).png>)

{% content-ref url="../../data/make-an-http-request.md" %}
[make-an-http-request.md](../../data/make-an-http-request.md)
{% endcontent-ref %}

