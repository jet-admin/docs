---
icon: shield-halved
---

# App and data permissions

Define access at each layer of the app, then test that the layers work together.

| Layer                      | Question to answer                                    |
| -------------------------- | ----------------------------------------------------- |
| Builder and administration | Who may change the app, membership, or configuration? |
| Pages and components       | Which screens and controls should each audience see?  |
| Actions                    | Who may create, update, delete, or run a workflow?    |
| Records                    | Which rows may the current user read or change?       |
| Data source or API         | Where is each request authorized?                     |

## Set up and verify access

1. Choose [roles](../teams-and-roles/built-in-roles.md) and [teams](../teams-and-roles/).
2. Define [page and action access](page-and-action-access.md).
3. Apply [record restrictions](record-access.md) using a trusted identity.
4. For customer portals, check [customer data isolation](customer-data-isolation.md).
5. Use [the test matrix](../overview/test-access.md) before publishing.

A hidden button or filtered table improves the interface but does not prove that the underlying request is forbidden. Validate authorization where the data request is handled.

[User and team properties](../members-users-and-groups/user-and-team-properties.md) can provide inputs to rules. Decide who may edit those values and what happens when a value is missing.
