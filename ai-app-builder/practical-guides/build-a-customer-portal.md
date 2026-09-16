# Build a customer portal

Build a read-only order portal where each signed-in customer can access only their own records.

## Prepare data and test accounts

Use Customers and Orders, with an explicit relationship from each order to its customer. Decide how a signed-in user maps to a customer. Prepare two invited test users and at least one order for each customer.

Configure the access rules with [App and data permissions](../../access-and-sharing/app-and-data-permissions/). A visual filter alone is not proof of customer isolation.

## Generate the portal

1. Select the connected source.
2. Adapt this prompt:

> Build a customer order portal using Customers and Orders. Use the configured relationship between the signed-in user and customer. Show only that customer's orders, with delivery status and a read-only detail view. Do not add update or refund actions.

3. Inspect the generated queries and record access configuration.
4. [Preview as the first invited user](../preview-and-troubleshoot/preview-as-an-invited-user.md), then the second.

## Verify isolation

| Check                              | Expected result                                  |
| ---------------------------------- | ------------------------------------------------ |
| Customer A opens the list          | Only A's orders appear.                          |
| Customer B opens the list          | Only B's orders appear.                          |
| A requests B's order directly      | Access is denied and B's record is not returned. |
| Anonymous visitor opens the portal | The configured authentication rule is enforced.  |

If isolation fails, correct the permission rules before sharing the app. Do not solve it only by hiding links or buttons.

Check the same cases with real sign-ins in the published app. Use [device previews](../preview-and-troubleshoot/control-app-preview.md) to review order details on mobile.
