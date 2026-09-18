---
hidden: true
---

# Cross-Instance Backup Restoration

For prerequisites, both transfer directions, and post-restore checks, use [Cross-Instance Backup & Restore](cross-instance-backup-and-restore.md). This shorter page retains the earlier walkthrough for reference.

Confirm the backup's scope, compatibility, and target recovery procedure before restoring. App configuration, connected database records, and external files can have different recovery mechanisms.

### Overview

The Cross-Instance Backup Restoration feature allows you to restore a backup from one Jet Admin instance to another, such as from an on-premise environment to the cloud.

#### Steps to Restore a Backup from a Different Instance

Follow these steps:

1. **Go to App Settings**
2. **Click on Restore Backup**
3. **Click on Advanced**
4. **Upload Your Backup File**
5. **Enter Your JET\_BRIDGE\_CLOUD\_TOKEN**
6. **Click on Restore Backup**

{% @arcade/embed url="https://app.arcade.software/share/Bz3otQQE2XIMEKj7ieCq" flowId="Bz3otQQE2XIMEKj7ieCq" %}

{% hint style="info" %}
**Important Notes**

* **JET\_BRIDGE\_CLOUD\_TOKEN**: This token is crucial when restoring a backup from a different Jet Admin instance. Ensure that you have this token ready before starting the restoration process.
* **Backup Compatibility**: Verify that the backup file is compatible with the instance you are restoring to, as differences in versions or configurations might affect the restoration.
{% endhint %}
