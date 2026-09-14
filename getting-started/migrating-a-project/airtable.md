---
description: >-
  Connect Airtable to Jet Admin to put a real app — with permissions and
  workflows — in front of a base your team has outgrown.
---

# Airtable

Airtable is the most common starting point for teams moving to Jet Admin: the base works, but you need proper permissions, a real interface for non-Airtable users, or data joined against another system.

{% hint style="info" %}
**You don't need a personal access token.** Airtable retired API keys in January 2024, but Jet Admin connects by signing in to Airtable directly — there's no token to create or paste.
{% endhint %}

## What you get

Every table you select from your base, with one **view** per table. Jet Admin can also generate CRUD pages for the tables you pick, giving you a working admin panel before you design anything.

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

Click **Choose tables**, select the tables you want, and pick a **view** for each one. Click **Add Resource**.

{% hint style="warning" %}
You can use **only one view per table**. A filtered view brings in only the records it shows — choose the **All** view unless you deliberately want the filter applied.
{% endhint %}
{% endstep %}

{% step %}
#### Choose your connection mode

Choose **Sync** to combine Airtable with Firebase, Google Sheets, a REST API or another source in the same tables. Choose **Direct** for live two-way edits against the base.
{% endstep %}

{% step %}
#### Generate your first pages

When prompted, pick the tables Jet Admin should generate an admin panel (CRUD pages) for. You can restyle or replace these later.
{% endstep %}
{% endstepper %}

## Switching views later

1. Click **Edit resource** from the resource's settings menu
2. Click **Choose tables**
3. Select the views you want for each table
4. Click **Update resource**

## Troubleshooting

**Records are missing from a table.** The selected view is filtered. Switch that table to the **All** view using the steps above.

**A new Airtable field isn't showing.** Run **More → Sync Structure** to pick up schema changes.

**I can't see the base I need.** Access was granted for a different base or workspace. Re-run **Add a base** and grant access to the right one.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}
