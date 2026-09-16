# Separate customer data

Use a two-customer test to verify that a portal does not expose one customer's data to another.

## Prepare a controlled example

Create two test customers, A and B, and one intended user for each. Give each customer a distinguishable test record. Use synthetic data so screenshots and test failures do not expose real customer information.

Associate each user with a trusted customer identifier using your application's identity model. If you use [user properties](../members-users-and-groups/user-and-team-properties.md), restrict who can edit the identifier.

## Run the isolation test

| Check                              | User A should observe                                    |
| ---------------------------------- | -------------------------------------------------------- |
| List and search                    | Only permitted customer A records.                       |
| Direct link to a customer B record | Access denied or no record returned.                     |
| Export or aggregate                | No unauthorized customer B data.                         |
| Update/delete customer B record    | Request denied; record unchanged.                        |
| Create a record for customer B     | Request denied or unauthorized ownership prevented.      |
| Missing customer identifier        | The explicit restricted behavior defined by your policy. |

Repeat as user B. Include linked records, uploaded files, background workflows, and APIs used by the app.

## Investigate failures

Trace the request to the data-access layer and check how the current identity is used. A customer ID supplied by the browser is not sufficient evidence of authorization.

Fix the underlying [record access rule](record-access.md) and repeat the same failed case. Preserve expected and actual results in your release review.

The existing [Classic customer portal guide](../../classic-app-builder/videos/build-apps-together/customer-portal.md) provides a builder-specific example; use the checks above for either builder.
