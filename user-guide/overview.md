# Choose where your data lives

Start with the records your app needs and who owns them. Jet Admin can read an existing database, API, or business service; store new tables in Jet Databases; or maintain a synchronized table from another source.

* **Existing source of truth:** connect it through [Data Sources](data-sources/). Check credentials, available records, and whether the app may write back.
* **New app data:** use [Jet Databases](jet-databases/) for tables you create and manage in Jet Admin.
* **A maintained copy:** use [Synced tables](synced-tables/) to bring a table from another source into Jet Databases and keep it refreshed. Review which system owns changes.

[Manage app data](data/) covers editing and relationships. For custom reads and updates, use [SQL queries and API requests](sql-queries-and-api-requests/). Before building an app, verify a few records and any write path with a safe account.
