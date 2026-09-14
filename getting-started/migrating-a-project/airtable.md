---
description: >-
  Connect Airtable to Jet Admin to put a real app — with permissions and
  workflows — in front of a base your team has outgrown.
---

# Airtable

Airtable is the most common starting point for teams moving to Jet Admin. Teams often keep their base and use Jet Admin for permissions, an interface for people who don't use Airtable, or joins with data from another system.

{% hint style="info" %}
Jet Admin connects through Airtable sign-in, so you don't need to create or paste a personal access token. Airtable retired API keys in January 2024.
{% endhint %}

## What you get

Jet Admin brings in each table you select from your base, using one view per table. It can also generate CRUD pages for those tables, so you have a working admin panel before designing your own pages.

## Before you start

* An Airtable account with access to the base
* Permission to grant a third-party app access to that base or workspace

## Connect Airtable

{% stepper %}
{% step %}
#### Add Airtable as a resource

In Jet Admin, click **Add Resource** from the **Data** section in the left menu, then choose **Airtable**.
{% endstep %}

{% step %}
#### Sign in to Airtable

Click **Sign In to Airtable**, then **Add a base**. Choose the base or workspace you need and click **Grant access**.
{% endstep %}

{% step %}
#### Choose tables and views

Click **Choose tables**, select the tables you want, and pick a view for each one. Click **Add Resource**.

{% hint style="warning" %}
You can use only one view per table. A filtered view brings in only the records it shows. Choose the **All** view unless you want that filter applied.
{% endhint %}
{% endstep %}

{% step %}
#### Choose your connection mode

Choose **Sync** to combine Airtable with Firebase, Google Sheets, a REST API or another source in the same tables. Choose **Direct** for live two-way edits against the base.
{% endstep %}

{% step %}
#### Generate your first pages

When prompted, select the tables for which Jet Admin should generate CRUD pages. You can restyle or replace the generated admin panel later.
{% endstep %}
{% endstepper %}

## Switching views later

1. Click **Edit resource** from the resource's settings menu
2. Click **Choose tables**
3. Select the views you want for each table
4. Click **Update resource**

## Troubleshooting

Records are missing from a table. The selected view is filtered. Switch that table to the **All** view using the steps above.

A new Airtable field isn't showing. Run **More → Sync Structure** to pick up schema changes.

I can't see the base I need. Access was granted for a different base or workspace. Re-run **Add a base** and grant access to the right one.

{% content-ref url="https://docs.jetadmin.io/getting-started/migrating-a-project" %}
[https://docs.jetadmin.io/getting-started/migrating-a-project](https://docs.jetadmin.io/getting-started/migrating-a-project)
{% endcontent-ref %}
