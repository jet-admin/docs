# Test data actions and user access

Use known test records and representative users to verify the app before sharing it.

## Prepare the checks

Create a record that can safely be changed and record its initial values. Identify at least one allowed user and one user who should be denied the action.

## Test a write action

1. Open the intended record in Preview.
2. Enter a recognizable test value.
3. Run the action once.
4. Confirm the UI shows success or an actionable error.
5. Inspect the source record to confirm exactly what changed.
6. Check an unrelated record remains unchanged.

If the response is unclear, inspect the source before retrying. A missing success message does not prove the write failed.

## Test access

Use [user preview](../preview-and-troubleshoot/preview-as-an-invited-user.md) to inspect pages and records. Then sign in with representative test accounts and verify access to the same data and actions.

| Scenario                                | Expected result                                      |
| --------------------------------------- | ---------------------------------------------------- |
| Staff updates an allowed ticket         | Only permitted fields on the selected record change. |
| A restricted user tries the same action | The operation is denied.                             |
| Customer A requests Customer B's record | The record is not exposed.                           |
| Invalid input is submitted              | No unintended record is created or changed.          |

For workflows, test the full run, including rejection or failure paths. Use [App and data permissions](../../access-and-sharing/app-and-data-permissions/) for rule configuration.

Next: [Preview and publish an AI app](preview-and-publish-an-ai-app.md).
