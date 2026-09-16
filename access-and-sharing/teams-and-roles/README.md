---
icon: users
---

# Teams and roles

Use teams to group people with a shared access requirement. Begin with the built-in role descriptions, then review any app-specific permissions.

## Recommended sequence

1. [Choose a built-in role](built-in-roles.md) for each audience.
2. [Create a team](create-and-manage-a-team.md) when a named group is useful.
3. [Invite users](../members-users-and-groups/invite-by-email.md) to the intended team.
4. Add [user or team properties](../members-users-and-groups/user-and-team-properties.md) only when an access rule or personalization needs them.
5. [Test access](../overview/test-access.md) with representative accounts.

## Design teams around tasks

For a ticket app, a support team might update tickets while a reviewer only reads them. A builder who changes the app needs a different access level from an agent who changes ticket data.

Write down the intended permissions for each team before configuration: pages, records, create/update/delete actions, and builder or administration access. A team name such as Support or Managers is a label; verify the actual permissions behind it.

When a person belongs to more than one team, test their effective access. Do not assume a restrictive team overrides a broader one unless you have verified the behavior in your app.
