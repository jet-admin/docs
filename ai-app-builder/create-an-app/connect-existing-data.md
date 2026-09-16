# Connect existing data

Before prompting for an app, connect the data it will use. You can use a database, an API, a business app, or a table in [Jet Databases](../../user-guide/jet-databases.md).

1. Pick the source of truth for the records the app must read or change. See Choose where your data lives.
2. Follow its [Data Sources](../../user-guide/data-sources/) guide to connect it. Check authentication and the scope of the credential.
3. Inspect the schema and a few sample records. Identify the table names, relationships, and fields you want shown in the app.
4. In your first prompt, name those actual sources and what users may do. Avoid asking for a write action until you know which source and account it will use.
5. Test a read and a safe update before sharing the app.

If an external table should be kept up to date inside Jet Databases, read [Synced tables](../../user-guide/synced-tables/). For queries and API requests, start with SQL queries and API requests.
