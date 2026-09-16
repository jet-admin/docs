---
description: In  this section you will learn about Users and Permissions
icon: user-group
---

# Manage members and access

Use the Users list to review who belongs to the app and the team associated with each person.

## Review a user

1. Open **Users** in the builder navigation, then the **Users** tab.
2. Search for the person's email or name.
3. Review their team and any properties used by access rules.
4. Compare the assignment with the [built-in role descriptions](../teams-and-roles/built-in-roles.md).
5. Test the resulting experience with the [invited-user preview](../../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) and, for sign-in checks, the person's test account.

## Change access deliberately

When changing membership through the controls available in your app, record the intended outcome first: builder access, app editing, or viewing only. Check all relevant team assignments; do not infer combined permissions from one team name.

For someone who leaves your organization, review app membership, identity-provider access, shared invitation links, and any separately issued credentials. Changing a property such as Status to Inactive is not by itself proof that sign-in or data access has been revoked.

After a change, check both a fresh sign-in and any existing session. Record the observed behavior instead of assuming immediate session termination.

## If the user sees the wrong app

Confirm the app and environment, published version, signed-in account, and team assignment. Use [sign-in troubleshooting](../authentication-and-sso/troubleshoot-sign-in.md) for login failures and [access tests](../overview/test-access.md) for permission failures.

For new people, continue with [email invitations](invite-by-email.md) or [invitation links](invite-with-a-link.md).
