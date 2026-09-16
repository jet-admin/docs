---
description: >-
  Bring a table from another database and keep it up to date automatically. One
  source of truth, used in as many Jet Databases as you need.
icon: arrows-rotate
---

# Synced tables

Bring a table from another database into Jet Databases and keep it up to date automatically. The original database remains the source of truth, so you can reuse its data across Jet Databases without maintaining separate copies by hand.

{% embed url="https://www.youtube.com/watch?v=l1jrrwlj0eU&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=25&ab_channel=JetAdmin" %}

## How synced tables work

A **sync connection** brings data from a supported source into Jet Databases. Jet Admin refreshes the synced data from the source, and your app uses that data to display records and run queries.

A **direct connection** accesses the source directly. To join data through synced tables, connect each source using a sync connection.

{% hint style="info" %}
Sync connections are available for a limited number of integrations. Check the connection options for your data source. If sync is unavailable, contact support to request it.
{% endhint %}

## Connect a source

When adding a supported data source, choose **Sync connection**. Follow the setup guide to connect the source and sync its structure.

{% content-ref url="create-a-sync-connection.md" %}
[create-a-sync-connection.md](create-a-sync-connection.md)
{% endcontent-ref %}

## Keep tables up to date

Updates from the source arrive on the external sync schedule. Updates between Jet Databases and the app interface happen in real time.

Open **Sync options** from the three-dot menu on your data source page to check the sync status and last sync time. You can pause syncing, run **Sync now**, and view sync events.

To change the external sync interval, contact Jet Admin support.

{% content-ref url="refresh-data-and-manage-sync.md" %}
[refresh-data-and-manage-sync.md](refresh-data-and-manage-sync.md)
{% endcontent-ref %}

## Join data from synced tables

Once your sources are synced, you can combine their data using SQL, including data from supported non-SQL sources. Create a **Virtual Collection** to define the query and use its results in your app.

For example, sync an `Orders` table from Airtable and a `Customers` table from Google Sheets. Join `Orders.Customer ID` to `Customers.ID` to display each order alongside the customer’s name and country.

{% content-ref url="join-data-from-multiple-sources.md" %}
[join-data-from-multiple-sources.md](join-data-from-multiple-sources.md)
{% endcontent-ref %}

{% hint style="warning" %}
A Virtual Collection is a read-only query result. It supports SELECT queries; it does not write changes back to the original sources. Syncing a source table and joining synced tables are separate operations.
{% endhint %}

## Follow the setup sequence

1. [Create a sync connection](create-a-sync-connection.md).
2. [Sync schema changes](syncing-schema-and-data.md) when source tables or fields change.
3. [Refresh data and manage sync](refresh-data-and-manage-sync.md).
4. [Join data from multiple sources](join-data-from-multiple-sources.md).
5. [Troubleshoot syncing](troubleshoot-syncing.md).
