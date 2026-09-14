---
description: >-
  Bring an existing Salesforce, HubSpot, Shopify, Stripe or Airtable project
  into Jet Admin — connect live to your data or sync it into Jet Tables, then
  build the app layer on top.
---

# Migrating a project to Jet Admin

Jet Admin connects to your existing systems and provides the interface, permissions, workflows, and agents your team uses. Your CRM, store, or base stays the system of record.

You don't need to export data or cut over to a new system. Jet Admin keeps using your existing source, so there's no separate migration copy to maintain.

{% hint style="info" %}
If you're rebuilding a prototype from another no-code app builder on your real data, start with [Quickstart](../../classic-app-builder/quickstart-2.md) and connect your database directly. There's nothing to export.
{% endhint %}

## Choose how your data arrives

Choose a connection type during setup based on how your app needs to use the data.

<table><thead><tr><th width="140">Connection</th><th>What it does</th><th>Choose this when</th></tr></thead><tbody><tr><td><strong>Direct</strong></td><td>Jet Admin reads and writes against the source in real time. Nothing is copied.</td><td>You need live two-way data, so editing a HubSpot deal in your app changes it in HubSpot. Direct connections are also required for write actions like Stripe refunds.</td></tr><tr><td><strong>Sync</strong></td><td>Jet Admin mirrors the source into <a href="../../user-guide/integrations/jet-tables/">Jet Tables</a>, its built-in SQL database, on a schedule.</td><td>You need to join data across sources, write SQL against a non-SQL source, or reduce load on the source API.</td></tr></tbody></table>

Use sync connections for [360 Data / Data Blending](../../user-guide/data-blending.md), such as joining Salesforce accounts to Stripe invoices in a single table. Check the limits below when choosing this mode.

{% hint style="warning" %}
Sync connections are available for a limited number of integrations. If your source doesn't support sync yet, use a direct connection and ask support to prioritise it.
{% endhint %}

## Choose your source

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Salesforce</strong></td><td>Accounts, Contacts, Opportunities via API key</td><td><a href="salesforce.md">salesforce.md</a></td></tr><tr><td><strong>HubSpot</strong></td><td>Contacts, Companies, Deals, Tickets via OAuth</td><td><a href="hubspot.md">hubspot.md</a></td></tr><tr><td><strong>Shopify</strong></td><td>Any Admin API object via a REST resource</td><td><a href="shopify.md">shopify.md</a></td></tr><tr><td><strong>Stripe</strong></td><td>Charges, invoices, subscriptions, and refunds</td><td><a href="stripe.md">stripe.md</a></td></tr><tr><td><strong>Airtable</strong></td><td>Any base, with generated CRUD pages</td><td><a href="airtable.md">airtable.md</a></td></tr></tbody></table>

If your source isn't listed, any of the 50+ [data sources](../../user-guide/integrations/) works the same way, and anything with an API can be connected as a [REST API](../../user-guide/integrations/rest-api/) or [GraphQL](../../user-guide/integrations/graphql.md) resource.

## What each source brings in

<table><thead><tr><th width="130">Source</th><th>Objects</th><th width="120">Auth</th><th width="90">Syncable</th></tr></thead><tbody><tr><td>Salesforce</td><td>Accounts, Contacts, Opportunities</td><td>API key</td><td>Yes</td></tr><tr><td>HubSpot</td><td>Contacts, Companies, Deals, Tickets</td><td>OAuth</td><td>Yes</td></tr><tr><td>Stripe</td><td>Charges, Customers, Disputes, Invoices, Plans, Products, Refunds</td><td>Secret key</td><td>Yes</td></tr><tr><td>Airtable</td><td>Selected tables, one view each</td><td>OAuth</td><td>Yes</td></tr><tr><td>Shopify</td><td>Any Admin API object</td><td>App token</td><td>No; direct only</td></tr></tbody></table>

{% hint style="info" %}
SQL databases such as MySQL and PostgreSQL connect directly and **cannot be synced or blended**.
{% endhint %}

## Then build the app

Once connected, all sources use the same app-building tools:

{% content-ref url="../../classic-app-builder/design-and-structure/components/" %}
[components](../../classic-app-builder/design-and-structure/components/)
{% endcontent-ref %}

{% content-ref url="../../user-guide/data-blending.md" %}
[data-blending.md](../../user-guide/data-blending.md)
{% endcontent-ref %}

{% content-ref url="../../agents/" %}
[agents](../../agents/)
{% endcontent-ref %}

For example, sync Salesforce and Stripe and blend accounts with invoices in one table. Build a table view and detail view, then add an [agent](../../agents/) so your team can ask questions about the blended data in plain language.

## Connection limits

{% hint style="danger" %}
Blended data is read-only. Blending creates virtual tables rather than copies, and only select operations are supported. Edits through a blended table aren't written back to the original source. If your app needs to write, use a direct connection or an individual synced table.
{% endhint %}

* Jet Admin support controls the sync interval for external updates from the source to Jet Tables. Internal updates from Jet Tables to your interface happen in real time. Contact support to change the external interval.
* SQL sources such as MySQL and PostgreSQL connect directly only and can't be blended.
* Some integrations don't support sync. Ask support to prioritise a source you need.
* Shopify uses a direct REST connection and won't appear in blending until a native integration ships.

You can check sync state at any time on the data source page: status (active or paused), last sync time, **Sync now** for a manual run, and **More → View Sync Events** for the history.

## FAQs

<details>

<summary>Does Jet Admin copy my data out of Salesforce, HubSpot or Stripe?</summary>

A sync connection mirrors your data into Jet Tables on a schedule. The source remains authoritative. A direct connection copies nothing; every read and write goes to the source live.

</details>

<details>

<summary>Can I connect the same source twice?</summary>

Yes. Add it once as a direct connection for writes and once as a sync connection for blending. They're separate resources with separate names.

</details>

<details>

<summary>What happens to my app if the source schema changes?</summary>

Run **More → Sync Structure** again to pick up new or renamed fields. Components bound to a field that no longer exists will need rebinding, so re-check views after a schema change upstream.

</details>

<details>

<summary>Will connecting Jet Admin change anything in my CRM or store?</summary>

Connecting and reading data leave the source untouched. Writes happen only through actions or workflows you explicitly build to write, using credentials with permission to do so.

</details>

<details>

<summary>Can I combine two sources in one table?</summary>

Yes, with sync connections on both, using [360 Data / Data Blending](../../user-guide/data-blending.md). The result is read-only.

</details>

<details>

<summary>My source isn't listed. Can I still use it?</summary>

Yes, if it has an API. Connect it as a [REST API](../../user-guide/integrations/rest-api/) or [GraphQL](../../user-guide/integrations/graphql.md) resource. [Ask AI](../../ask-ai.md) can generate the requests from a curl command or a link to the API's documentation.

</details>

{% content-ref url="../../troubleshoot.md" %}
[troubleshoot.md](../../troubleshoot.md)
{% endcontent-ref %}
