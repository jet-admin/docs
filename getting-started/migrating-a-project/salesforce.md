---
description: >-
  Connect Salesforce to Jet Admin to build apps on your Accounts, Contacts and
  Opportunities — live, or synced into Jet Tables.
---

# Salesforce

Use Jet Admin to build apps on your Salesforce org while keeping Salesforce as the system of record.

{% hint style="success" %}
Jet Admin reads your Salesforce data. Connecting it doesn't modify anything in your org.
{% endhint %}

## What you get

Jet syncs the following Salesforce objects:

* Accounts
* Contacts
* Opportunities

Jet Admin preserves relationships between these objects, so an Account resolves to its Contacts and Opportunities in the Data Editor.

{% hint style="info" %}
Custom objects aren't part of the standard sync. To access them, add a [REST API resource](../../user-guide/data-sources/apis/rest-api/) pointed at the Salesforce REST API alongside this one.
{% endhint %}

## Before you start

* A Salesforce account with access to the objects you need
* If your org has a sandbox, connect that first and switch to production once the app works

## Connect Salesforce

{% stepper %}
{% step %}
#### Add Salesforce as a resource

In Jet Admin, open **Data → Add Resource** and select **Salesforce**.
{% endstep %}

{% step %}
#### Sign in to Salesforce

Click **Sign in to Salesforce** and complete the OAuth prompt. Jet Admin doesn't need an API key — Salesforce handles authentication and permissions for you.
{% endstep %}

{% step %}
{% @arcade/embed flowId="Kol8IrH2FwhYCXUemSad" url="https://app.arcade.software/share/Kol8IrH2FwhYCXUemSad" %}

#### Choose your connection mode

Choose **Sync** to blend Salesforce with another source. Choose **Direct** for writes that update Salesforce immediately. See [Choosing a connection mode](https://docs.jetadmin.io/getting-started/migrating-a-project) if you're unsure.
{% endstep %}

{% step %}
#### Sync the structure

Click the **More** icon on the resource, then **Sync Structure**. Accounts, Contacts and Opportunities appear in the Data Editor.
{% endstep %}

{% step %}
#### Check the data

Open each table in the Data Editor and check the records and field types before building your app.
{% endstep %}
{% endstepper %}

## Troubleshooting

Tables are empty after connecting. The structure synced but the data hasn't. Run **Sync now**, then check **More → View Sync Events** for errors.

An object I need is missing. Only Accounts, Contacts and Opportunities are part of the standard sync. Custom objects need a REST API resource.

Fields changed in Salesforce and my app broke. Run **More → Sync Structure** again, then rebind any component pointing at a renamed field.

{% content-ref url="https://docs.jetadmin.io/getting-started/migrating-a-project" %}
[https://docs.jetadmin.io/getting-started/migrating-a-project](https://docs.jetadmin.io/getting-started/migrating-a-project)
{% endcontent-ref %}
