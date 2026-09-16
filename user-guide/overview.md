---
icon: lightbulb
---

# Choose where your data lives

Choose the connection based on where your records belong and how your app needs to use them.

| Option            | Where records live                           | Use it when                                            | Check before editing                                         |
| ----------------- | -------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| Jet Databases     | A database hosted by Jet Admin               | You need new tables for your app                       | Field types, required values, and record permissions         |
| Direct connection | Your existing database or service            | You want to work with an existing source directly      | The connector's supported operations and account permissions |
| Sync connection   | Source records are copied into Jet Databases | You need synced data or joins across supported sources | Refresh schedule and the connector's write behavior          |

A sync connection does not by itself guarantee two-way writes. The original source remains the source of truth; confirm where an edit is saved before enabling it in your app. A Virtual Collection is a read-only query result.

## Start with a task

* [Connect your first data source](data-sources/connect-your-first-data-source.md)
* [Create a table](jet-databases/create-a-table.md)
* [Set up synced tables](synced-tables/)
* [Manage records and fields](data/)
* [Write SQL queries and API requests](sql-queries-and-api-requests/)
* [Upload and manage files](data/file-storage.md)

After connecting, compare several records with the source. If your app will update data, test one disposable record and verify the saved value in the system that owns it.
