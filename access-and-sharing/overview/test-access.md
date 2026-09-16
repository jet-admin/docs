# Test access before publishing

Use representative accounts to verify the access policy, including actions that must fail.

**Before you start:** use synthetic test records, identify the app environment and version, and write the expected result for each role.

## Test matrix

| Test                                 | What to verify                                              |
| ------------------------------------ | ----------------------------------------------------------- |
| Sign-in with intended account        | Identity and membership are correct.                        |
| Sign-in with unintended account      | Access follows the intended rejection or onboarding policy. |
| Allowed page and record              | Intended content is available.                              |
| Restricted page or direct record URL | Unauthorized content is unavailable.                        |
| Allowed create/update                | Only the intended test record changes.                      |
| Denied create/update/delete          | Request fails and data remains unchanged.                   |
| Search, export, and related records  | No data outside the permitted scope.                        |
| Workflow or API action               | The same identity and record restrictions apply.            |
| User with missing access property    | The defined restricted behavior occurs.                     |
| Membership or role change            | A fresh sign-in and existing session behave as intended.    |

## Run and record

1. Use [invited-user preview](../../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) to inspect pages and controls.
2. Sign in separately as each test user to verify authentication and published-app behavior.
3. Exercise allowed and denied operations on test data.
4. Check the resulting records and available logs.
5. Record expected result, actual result, and evidence for each case.
6. Fix failures and repeat the affected tests before release.

For multi-customer apps, run [the two-customer isolation test](../app-and-data-permissions/customer-data-isolation.md). For action behavior, see [the AI App Builder action testing guide](../../ai-app-builder/test-and-publish/check-data-actions-and-user-access.md).
