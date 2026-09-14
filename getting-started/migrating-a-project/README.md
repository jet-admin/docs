---
description: >-
  Bring an existing Salesforce, HubSpot, Shopify, Stripe or Airtable project
  into Jet Admin — connect live to your data or sync it into Jet Tables, then
  build the app layer on top.
---

# Migrating a project to Jet Admin

You don't move off your existing systems to use Jet Admin. You connect to them, and Jet Admin becomes the app layer on top — the interface, the permissions, the workflows, and the agents your team actually works in. Your CRM, store, or base stays the system of record.

That makes migrating to Jet Admin cheaper than it sounds: there's no export, no data cutover, and nothing to keep in step afterwards.

{% hint style="info" %}
**Coming from a no-code app builder instead?** If you built a prototype elsewhere and want to rebuild it on your real data, start with [Quickstart](../quickstart-2.md) and connect your database directly. There's nothing to export.
{% endhint %}

## Choose how your data arrives

Before you connect anything, decide which of the two connection types you need. You're asked to choose during setup, and it determines what you can do afterwards.

<table><thead><tr><th width="140">Connection</th><th>What it does</th><th>Choose this when</th></tr></thead><tbody><tr><td><strong>Direct</strong></td><td>Jet Admin reads and writes against the source in real time. Nothing is copied.</td><td>You need live two-way data — editing a HubSpot deal in your app should change it in HubSpot. Also required for write actions like Stripe refunds.</td></tr><tr><td><strong>Sync</strong></td><td>Jet Admin mirrors the source into <a href="../../user-guide/integrations/jet-tables/">Jet Tables</a>, its built-in SQL database, on a schedule.</td><td>You need to join data across sources, write SQL against a non-SQL source, or reduce load on the source API.</td></tr></tbody></table>

Sync is what makes [360 Data / Data Blending](../../user-guide/data-blending.md) possible — joining Salesforce accounts to Stripe invoices in a single table, for example. Read the limits below before you commit to it.

{% hint style="warning" %}
Sync connections are available for a **limited number of integrations**. If the source you need isn't syncable yet, ask support to prioritise it — and use a direct connection in the meantime.
{% endhint %}

## Choose your source

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Salesforce</strong></td><td>Accounts, Contacts, Opportunities via API key</td><td><a href="salesforce.md">salesforce.md</a></td></tr><tr><td><strong>HubSpot</strong></td><td>Contacts, Companies, Deals, Tickets via OAuth</td><td><a href="hubspot.md">hubspot.md</a></td></tr><tr><td><strong>Shopify</strong></td><td>Any Admin API object via a REST resource</td><td><a href="shopify.md">shopify.md</a></td></tr><tr><td><strong>Stripe</strong></td><td>Charges, invoices, subscriptions — with refunds</td><td><a href="stripe.md">stripe.md</a></td></tr><tr><td><strong>Airtable</strong></td><td>Any base, with generated CRUD pages</td><td><a href="airtable.md">airtable.md</a></td></tr></tbody></table>

Not listed? Any of the 50+ [data sources](../../user-guide/integrations/) works the same way, and anything with an API can be connected as a [REST API](../../user-guide/integrations/rest-api/) or [GraphQL](../../user-guide/integrations/graphql.md) resource.

## What each source brings in

<table><thead><tr><th width="130">Source</th><th>Objects</th><th width="120">Auth</th><th width="90">Syncable</th></tr></thead><tbody><tr><td>Salesforce</td><td>Accounts, Contacts, Opportunities</td><td>API key</td><td>Yes</td></tr><tr><td>HubSpot</td><td>Contacts, Companies, Deals, Tickets</td><td>OAuth</td><td>Yes</td></tr><tr><td>Stripe</td><td>Charges, Customers, Disputes, Invoices, Plans, Products, Refunds</td><td>Secret key</td><td>Yes</td></tr><tr><td>Airtable</td><td>Selected tables, one view each</td><td>OAuth</td><td>Yes</td></tr><tr><td>Shopify</td><td>Any Admin API object</td><td>App token</td><td>No — direct only</td></tr></tbody></table>

{% hint style="info" %}
SQL databases such as MySQL and PostgreSQL connect directly and **cannot be synced or blended**.
{% endhint %}

## Then build the app

Once your data is connected, the build is the same regardless of where the data came from:

{% content-ref url="../../user-guide/components/" %}
[components](../../user-guide/components/)
{% endcontent-ref %}

{% content-ref url="../../user-guide/data-blending.md" %}
[data-blending.md](../../user-guide/data-blending.md)
{% endcontent-ref %}

{% content-ref url="../../agents/" %}
[agents](../../agents/)
{% endcontent-ref %}

A common pattern: sync Salesforce and Stripe, blend accounts against invoices into one table, build a table and detail view over it, then put an [agent](../../agents/) on top so your team can ask questions about the blended data in plain language.

## Limits worth knowing before you commit

{% hint style="danger" %}
**Blended data is read-only.** Blending creates virtual tables, not copies. You can only run select operations against a blended table, and edits made through it are **not written back** to the original source. If your app needs to write, build it on a direct connection or on the individual synced table.
{% endhint %}

* **Sync interval is set by Jet Admin, not by you.** Syncing has two halves: _external updates_ (source → Jet Tables) run on an interval only Jet Admin support can change; _internal updates_ (Jet Tables → your interface) are real-time. Contact support if you need a different external interval.
* **SQL sources can't be blended.** MySQL, PostgreSQL and similar connect directly only.
* **Sync isn't available for every integration.** Ask support to prioritise a source if you need it.
* **Shopify is a direct REST connection**, so it won't appear in blending until a native integration ships.

You can check sync state at any time on the data source page: status (active or paused), last sync time, **Sync now** for a manual run, and **More → View Sync Events** for the history.

## FAQs

<details>

<summary>Does Jet Admin copy my data out of Salesforce, HubSpot or Stripe?</summary>

Only if you choose a sync connection — and then it mirrors into Jet Tables on a schedule, with the source staying authoritative. A direct connection copies nothing; every read and write goes to the source live.

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

Not by connecting. Reads leave the source untouched. Writes only happen where you explicitly build an action or workflow that writes — and only if the credential you supplied has permission to do it.

</details>

<details>

<summary>Can I combine two sources in one table?</summary>

Yes, with sync connections on both, using [360 Data / Data Blending](../../user-guide/data-blending.md). Remember the result is read-only.

</details>

<details>

<summary>My source isn't listed. Can I still use it?</summary>

Yes, if it has an API. Connect it as a [REST API](../../user-guide/integrations/rest-api/) or [GraphQL](../../user-guide/integrations/graphql.md) resource. [Ask AI](../../ask-ai.md) can generate the requests from a curl command or a link to the API's documentation.

</details>

{% content-ref url="../../troubleshoot.md" %}
[troubleshoot.md](../../troubleshoot.md)
{% endcontent-ref %}
