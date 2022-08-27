---
description: >-
  This guide explains how to quickly connect Xano back-end to a Jet Admin
  front-end.
---

# Xano

Xano is the fastest way to build a powerful, scalable backend for your app without code.

### Connect the API queries to Jet Admin <a href="#step-2-connect-the-database-to-appsmith" id="step-2-connect-the-database-to-appsmith"></a>



Choose a Rest API database from the list of available data sources:

<figure><img src="../../.gitbook/assets/rest api.jpg" alt=""><figcaption></figcaption></figure>

Let's start with implementing **Rest API**, select it from the list of available resources, and specify the general information that will use for all API requests for this resource:&#x20;

* **Resource name** – unique name that indicates API resource in Jet Admin.
* **Base URL** – URL that will use for all requests for this resource (if you want to use different URL, create different resources for each URL).

<figure><img src="../../.gitbook/assets/xano1.jpg" alt=""><figcaption></figcaption></figure>



Create a new Collection with your Xano's query:

<figure><img src="../../.gitbook/assets/xano2.jpg" alt=""><figcaption></figcaption></figure>

{% content-ref url="../data/make-an-http-request.md" %}
[make-an-http-request.md](../data/make-an-http-request.md)
{% endcontent-ref %}
