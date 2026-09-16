# Troubleshoot syncing

Identify whether the problem concerns a connection, schema, or record values.

| What you see                     | What to do                                                                                          |
| -------------------------------- | --------------------------------------------------------------------------------------------------- |
| New tables or fields are missing | Confirm access in the source, then [sync schema changes](syncing-schema-and-data.md).               |
| Fields exist but values are old  | Check sync status and last-sync time, then [run a manual refresh](refresh-data-and-manage-sync.md). |
| Sync is paused                   | Review the status and sync controls for the resource.                                               |
| Sync fails                       | Inspect sync events and the provider's connection requirements.                                     |
| Only some records are missing    | Check the source view, filters, and selected tables.                                                |
| A joined result is empty         | Confirm both sources have synced and the join keys match.                                           |

## Verify a refresh

Choose a known source record and note its ID and a field value. Run **Sync now** where available, then compare the same record in Jet Admin after the sync completes.

Schema refresh and data refresh solve different problems. A successful sync does not change the access granted by your source credentials.

## Get help

See [A data resource is failing to sync](../../faq-and-troubleshooting/a-data-resource-is-failing-to-sync.md). Include the resource, environment, exact error, last successful sync time, and one example record ID. Remove credentials from screenshots and logs.
