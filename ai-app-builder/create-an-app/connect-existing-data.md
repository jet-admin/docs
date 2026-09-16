# Connect existing data

Connect a database, API, business application, or Jet Database before asking the assistant to build on its records.

## Connect and inspect

1. Choose the source of truth for your records.
2. Open **Data** and follow the relevant [Data Sources guide](../../user-guide/data-sources/).
3. Check authentication and the access granted to the connection.
4. Inspect the tables, field types, relationships, and sample records.
5. Open the assistant and [select the connected resource](../ai-assistant/select-data-sources.md).

Connection setup makes the source available to the project. Resource selection tells the assistant which connected source to use for the task.

## Example: Tickets and Customers

Identify which Tickets field refers to a customer and which Customers field is its identifier. Use those exact names in your prompt rather than asking the assistant to guess a relationship.

Start with a read-only request and compare a displayed record with the source. Add a write action only after confirming which source and account will receive it.

## If data is missing

Check the source connection in Data, the credential's scope, and whether the schema includes the field you named. For a synchronized table, check its synchronization status and settings.

Next: [Write your first prompt](write-a-useful-prompt.md).
