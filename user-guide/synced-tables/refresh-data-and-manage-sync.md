---
description: Refresh record values, inspect sync status, and review sync events.
---

# Refresh data and manage sync

Use these controls when existing record values have changed. For new tables or columns, use [Sync schema changes](syncing-schema-and-data.md).

## Understand the two refresh stages

```mermaid
flowchart LR
  A["Original source"] -->|"External sync schedule"| B["Jet Tables"]
  B -->|"Internal updates"| C["App interface"]
```

External updates bring changes from the source into Jet Tables. Internal updates propagate Jet Tables changes to the interface. A current interface does not mean the source was just refreshed.

## Refresh records

1. Open the resource in **Data**.
2. Check whether syncing is **active** or **paused**, and note the last sync time.
3. Use **Sync now** to request a manual refresh.
4. Review the resulting status and last sync time.
5. Reopen a known record and compare its value with the source.

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FuJCDzHflNQRS1Fo95r9F%2FScreenshot%202024-12-26%20163715.png?alt=media&#x26;token=816c2250-9eaf-4376-bb67-604214d47b79" alt="Sync status, pause control, and Sync now on the data source page"><figcaption><p>Sync status, pause control, and Sync now on the data source page</p></figcaption></figure>

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F6IJTL8Egx1FsPA3iZEgR%2Ftime.png?alt=media&#x26;token=e62d273d-2399-42c9-952f-8a6417f95e26" alt="Last sync date and time beside the resource status"><figcaption><p>Last sync date and time beside the resource status</p></figcaption></figure>

## Check options and events

Open the three-dot menu and select **Sync options** to inspect the connection settings. To change the external sync interval, contact Jet Admin support.

{% @arcade/embed url="https://app.arcade.software/share/Nqylpaze42V2N99aCE19" flowId="Nqylpaze42V2N99aCE19" %}

For diagnostics, open **More → View Sync Events** and inspect the relevant event details.

{% @arcade/embed url="https://app.arcade.software/share/d5jg7wZ7Ubdzaj91ffn7" flowId="d5jg7wZ7Ubdzaj91ffn7" %}

If records still differ, follow [Troubleshoot syncing](troubleshoot-syncing.md).
