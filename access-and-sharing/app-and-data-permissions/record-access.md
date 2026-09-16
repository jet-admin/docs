# Restrict access to records

Define which records an authenticated user may read or change. Enforce that decision in the data-access layer that handles the request.

## Define the rule

For a customer portal, an example policy is: a user may access a ticket only when the ticket's customer ID matches the user's trusted customer ID.

Before implementing that policy, identify:

* Where the authenticated identity comes from.
* Where its customer ID is stored and who can edit it.
* Which queries and actions access tickets.
* How missing or invalid customer IDs are handled.

## Apply the rule consistently

Cover list queries, individual record reads, search, counts, exports, create, update, delete, and any workflows that operate on the same data. A page filter alone does not establish authorization for these other paths.

For writes, verify both the existing record's ownership and any submitted ownership values. Do not let a user assign a new record to an unauthorized customer or move an existing record outside their permitted scope.

The exact implementation depends on the resource, API, and app architecture. Use its supported authorization mechanism and test the result; do not infer enforcement from generated UI code.

## Verify with two users

Create test identities for two different customers and test records for each. Confirm each identity can access its own permitted records and cannot read or modify the other's records, including a direct record request.

Repeat with a missing customer ID. The intended restricted behavior should be explicit. Use [the test matrix](../overview/test-access.md) to record results and [customer data isolation](customer-data-isolation.md) for a complete portal review.
