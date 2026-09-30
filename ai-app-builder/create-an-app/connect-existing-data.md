# Connect existing data

Connect a database, API, business application, or Jet Database before asking the assistant to build on its records.

## Connect and inspect

1. Choose the source of truth for your records.
2. Open **Data** and follow the relevant [Data Sources guide](../../user-guide/data-sources/).
3. Check authentication and the access granted to the connection.
4. Inspect the tables, field types, relationships, and sample records.
5. Open the assistant and select the connected resource.

Connection setup makes the source available to the project. Resource selection tells the assistant which connected source to use for the task.

## Connect during app planning

In the AI App Builder preview, you can name the resource in your initial request. When access is needed, the assistant presents a connection request before planning the app.

1. Select the requested resource and complete its connection or access flow.
2. Check that the assistant has identified the expected collections and fields.
3. Answer any questions about the app's users and purpose.
4. Review the proposed plan and confirm before generation begins.

![Assistant connecting Firebase before planning the app](https://250870895-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F8xy7P3kSppSd57K7pcpL%2Fuploads%2F9BAM55KrqOY56rTy1m7Q%2Fsept29-connect-resource.jpg?alt=media)

If the plan does not reflect your data, ask the assistant to inspect the selected resource and revise the plan before building.

## Example: Tickets and Customers

Identify which Tickets field refers to a customer and which Customers field is its identifier. Use those exact names in your prompt rather than asking the assistant to guess a relationship.

Start with a read-only request and compare a displayed record with the source. Add a write action only after confirming which source and account will receive it.

## If data is missing

Check the source connection in Data, the credential's scope, and whether the schema includes the field you named. For a synchronized table, check its synchronization status and settings.

Next: Write your first prompt.
