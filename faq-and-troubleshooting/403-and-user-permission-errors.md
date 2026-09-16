# A user gets 403 or cannot access a page

A 403 or access-denied message means you need to check the affected user's access to the particular app, page, or action.

## Check the affected account and role

1. Confirm the user is signing in to the intended app and environment with the expected email address.
2. Ask an administrator to compare the user's assigned groups, page access, and data/action permissions with the intended role.
3. Save any work, sign out, and sign in again. A fresh session can help when permissions have changed; it does not repair an incorrect role.
4. Retest the same page and action using the affected user's account.

If one user succeeds and another fails, compare their actual assignments rather than relying only on a role's display name.

See [App and data permissions](https://docs.jetadmin.io/access-and-sharing/app-and-data-permissions).

## Still getting 403?

Send support the app URL, environment, affected page/action, expected role, and time of the failed attempt. State whether signing in again changed the result and whether other users are affected.

Share the error text or a sanitized screenshot, not session cookies or JWT tokens. Avoid granting administrator access as a workaround for an unexplained permission difference.

_Last reviewed: September 16, 2026._
