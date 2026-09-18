---
description: >-
  This guide explains how to move (restore) backups between JetAdmin Cloud and
  JetAdmin On‑Premise environments in both directions.
---

# Cross-Instance Backup & Restore

## Before you start

Confirm the source and target app/environment, platform compatibility, backup contents, and a tested recovery path for the target. An app backup is not proof that every connected database record, file, or credential is included. Arrange database/storage recovery separately where needed.

The flows below are deployment-specific reference instructions. Check the controls and token requirements of your installed version before restoring. Use a test target first; this documentation update did not execute a cross-instance restore.

### Restore Backup from On‑Prem → Cloud

Use this flow when you want to transfer the contents included in an **On‑Prem backup into Jet Admin Cloud**.

In this case, you first download or export a backup from your On‑Prem system, then upload it into the Cloud instance.

{% hint style="info" %}
Before starting, make sure you have the **JET\_BRIDGE\_CLOUD\_TOKEN** from your On‑Prem server (`jet-onpremise/.env`).
{% endhint %}

{% hint style="warning" %}
Note: Before restoring into Cloud, it is strongly recommended to create a backup of your current Cloud environment. A restore can replace target configuration or included data. Keep a compatible target backup and verify that your recovery procedure works before relying on it.
{% endhint %}

#### Steps in Cloud App (Restore Backup)

Go to App Settings

Click on Restore Backup

Upload your backup file

Click on Advanced

Enter your JET\_BRIDGE\_CLOUD\_TOKEN (the same token from the On‑Prem `.env` file)

Click on Restore Backup

{% @arcade/embed url="https://app.arcade.software/share/Bz3otQQE2XIMEKj7ieCq" flowId="Bz3otQQE2XIMEKj7ieCq" %}

### Restore Backup from Cloud → On‑Prem

Use this flow when you want to transfer the contents included in a **Cloud backup into your On‑Prem installation**.

Before starting, make sure you have the **JET\_BRIDGE\_CLOUD\_TOKEN** from your On‑Prem server.

Open this file and copy the value of `JET_BRIDGE_CLOUD_TOKEN`. You do not need to generate or configure this token manually.

#### Steps in Cloud App (Download Backup)

Go to Download Backup

Click on Advanced Settings

Enter your JET\_BRIDGE\_CLOUD\_TOKEN (from the On‑Prem `.env` file)

Click on Download Backup

Wait until the backup file is downloaded.

#### Steps in On‑Prem App (Restore Backup)

Go to App Settings

Go to Restore Backup

Upload the downloaded backup file

Click on Advanced Settings

Leave the token field empty (the system will use the token from `.env` automatically)

Click on Restore Backup

After the process finishes, verify the included configuration and data on the target. Check external resource connections, file access, and permissions independently.

{% hint style="warning" %}
### Important: JET\_BRIDGE\_CLOUD\_TOKEN

When JetAdmin On‑Prem is deployed, a bridge token is automatically generated and stored in the environment file:

`jet-onpremise/.env`

Example:

`JET_BRIDGE_CLOUD_TOKEN=jet_bridge_xxxxx`

You do **not** need to create this token manually. The same token is used for:

* Downloading backups from Cloud to On‑Prem
* Restoring On‑Prem backups into Cloud

Always keep this token private and do not share it outside your organization.
{% endhint %}

{% hint style="success" %}
### Useful Tips and Best Practices

Before any restore, always create a backup of the **target system** (Cloud or On‑Prem). A restore can replace target configuration or included data; confirm the scope before proceeding.

If a restore fails, first check:

* That the token in the UI matches the token in `jet-onpremise/.env`
* That the On‑Prem service was restarted after any `.env` change
{% endhint %}

## Verify the restored target

1. Confirm the target app, environment, and platform version.
2. Open representative pages and test read access to their resources.
3. Check any included records/files against the backup's documented scope.
4. Test an allowed and a denied action with dedicated test identities.
5. Confirm the intended release at its app URL before inviting users to rely on it.

If the result is incomplete, inspect the restore error and included backup scope before retrying. Do not assume repeating a restore reverses partial effects. See [Version History and recovery](../).
