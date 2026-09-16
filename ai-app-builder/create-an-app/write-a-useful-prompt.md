# Write your first prompt

A useful first prompt names the users, data, screens, and allowed actions. Use actual table and field names where possible. Start with one job you can check against a few test records.

For example:

> Build an order operations app for support staff. Use the Orders and Customers tables. Show open orders in a filterable table and a detail screen with the customer record. Allow support staff to update fulfillment status. Keep refund actions available only to managers.

Before generating, connect [the source](../../user-guide/data-sources/) or start with [Jet Databases](../../user-guide/jet-databases/). If the prompt uses a table the app cannot read, clarify the connection first. After generation, compare filters and actions to the source schema. Ask for one revision at a time; for example, “Add a status filter to Orders,” then check the result. Continue with [Review generated pages and logic](../refine-an-app/review-and-refine.md).
