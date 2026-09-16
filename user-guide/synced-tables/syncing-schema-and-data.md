---
description: Sync allows you to push all of your data to Jet Tables
---

# Syncing Schema and Data

If you make any changes to your schema or data, such as adding new tables or fields, this will not appear immediately in Jet. Run a manual sync directly in Jet to see the changes.

## Run Schema Sync <a href="#run-schema-sync-0-0" id="run-schema-sync-0-0"></a>

Jet automatically doesn't sync the schema structure, you can manually run a schema sync as an admin whenever you need in order to see changes reflected straight away.

<figure><img src="../../.gitbook/assets/sync.gif" alt=""><figcaption></figcaption></figure>

### Run Schema Sync for Rest API

<figure><img src="../../.gitbook/assets/apisync.gif" alt=""><figcaption></figcaption></figure>

## Run Data sync <a href="#run-data-sync-0-1" id="run-data-sync-0-1"></a>

When you or your users make changes to your data in Jet, those changes are reflected immediately in your data source.

When updates are made directly in your external data source - i.e. Airtable, Google Sheets, Stripe etc - they will be visible in Jet up to **5 minutes** depending on the sync interval. This is because we re-cache the data every N minutes. You can manually run **`Sync now`** or specify the **N sync interval.**

### **Sync now**

<figure><img src="../../.gitbook/assets/syncnow.gif" alt=""><figcaption></figcaption></figure>

### Specify N sync interval for Rest API

<figure><img src="../../.gitbook/assets/apisyncinterval.gif" alt=""><figcaption></figcaption></figure>
