---
description: >-
  This guide explains how to quickly connect Webflow CMS back-end to a Jet Admin
  front-end.
---

# Webflow

### Step 1: Get your API key <a href="#step-1-set-up-your-backend-on-supabase" id="step-1-set-up-your-backend-on-supabase"></a>

Go to Webflow [Dashboard](https://webflow.com/dashboard) > **Settings**

<figure><img src="../../.gitbook/assets/prj_settings.jpg" alt=""><figcaption></figcaption></figure>

Go to > **Integrations**

<figure><img src="../../.gitbook/assets/prj_integrations.jpg" alt=""><figcaption></figcaption></figure>

Scroll down to **API Access** > **Generate API token**

<figure><img src="../../.gitbook/assets/prJ_api.jpg" alt=""><figcaption></figcaption></figure>

### Step 2: Connect the API queries to Jet Admin <a href="#step-2-connect-the-database-to-appsmith" id="step-2-connect-the-database-to-appsmith"></a>

Choose a Rest API database from the list of available data sources:

<figure><img src="../../.gitbook/assets/rest api.jpg" alt=""><figcaption></figcaption></figure>

Let's start with implementing **Rest API**, select it from the list of available resources, and specify the general information that will use for all API requests for this resource:&#x20;

* **Resource name** – unique name that indicates API resource in Jet Admin.
* **Base URL** – URL that will use for all requests for this resource (if you want to use different URL, create different resources for each URL).

<figure><img src="../../.gitbook/assets/Untitled 2.jpg" alt=""><figcaption></figcaption></figure>

Create a new Collection with your Webflow's query:

<figure><img src="../../.gitbook/assets/webflow_api.jpg" alt=""><figcaption></figcaption></figure>

{% content-ref url="../data/make-an-http-request.md" %}
[make-an-http-request.md](../data/make-an-http-request.md)
{% endcontent-ref %}
