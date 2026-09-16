# Preview as an invited user

Preview the app on behalf of a specific invited user to inspect their experience.

## Before you begin

Invite the test user to the project and configure their intended role and access. Prepare records they should see and records they should not see.

## Choose a user

1. Open **Preview**.
2. Click the current user name in the Preview toolbar, beside **Theme**.
3. Search for and select the invited user.
4. Confirm the toolbar shows the intended user.
5. Open the pages and actions that person needs to use.

The selector may also offer **Anonymous** for checking the experience of someone who is not signed in.

## Check the result

| Test                           | Expected result                                      |
| ------------------------------ | ---------------------------------------------------- |
| Open an allowed page           | The user can reach it and read the intended records. |
| Open a restricted page         | Access follows the configured rule.                  |
| Open another customer's record | Customer isolation remains enforced.                 |
| Try a restricted action        | The action is rejected, not merely hidden.           |

Switch back to your own user when finished.

User preview helps inspect the app, but a hidden button alone does not establish that data permissions are enforced. Repeat critical checks by signing in as the test user in the published app.

If a user is absent from the selector, check their invitation and membership in **Users**. For unexpected records, inspect the app's data and access rules.

Next: [Test data actions and user access](../test-and-publish/check-data-actions-and-user-access.md).
