---
description: Refresh a resource's schema after adding or changing tables and fields.
---

# Sync schema changes

Refresh a resource's schema after adding or changing tables or fields in the source. A schema refresh updates the structure Jet Admin discovers; refreshing record values is a separate task.

## Before you start

Make the schema change in your source first. Use an administrator account in Jet Admin, and check that the resource's credentials can access the affected tables and fields.

## Refresh the schema

1. Open **Data** and select the resource you changed.
2. Open the resource's **More** menu and select **Sync Structure**. Some resource interfaces label the schema-refresh control **Sync**.

<figure><img src="../../.gitbook/assets/S18-sync-structure-menu.jpg" alt="HubSpot resource menu with Sync Structure"><figcaption><p>Select Sync Structure from the resource menu. This image shows the command, not a completed refresh.</p></figcaption></figure>

3. After the refresh, open the affected table or collection.
4. Check that the new table or field appears.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2Fpqe6jzr8mZoPGo2qGlw6%2Fsync.gif?alt=media&#x26;token=34d29411-f8fa-4eba-8542-706e5211520d" alt="Resource menu showing the schema synchronization action"><figcaption></figcaption></figure>

### REST API resources

Open the REST API resource and use its schema-sync control after changing the structure exposed by the API.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FBmwZhDlNs0iNfm3LMmTz%2Fapisync.gif?alt=media&#x26;token=bbf2a57d-0f5c-417e-838b-7793108e1dea" alt="Schema synchronization in a REST API resource"><figcaption></figcaption></figure>

## If a table or field is still missing

Check that the change exists in the source and that the credentials used by Jet Admin can access it. Confirm that you refreshed the intended resource.

For further checks, see [A data resource is failing to sync](../../faq-and-troubleshooting/a-data-resource-is-failing-to-sync.md).

## Refresh record values

If the table structure is correct but record values are stale, use **Sync now** for a synced connection. See [Sync Options](refresh-data-and-manage-sync.md) for sync status, manual refresh, events, and interval settings.
