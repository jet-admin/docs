# Check data actions and user access

Use test records and representative accounts to verify an app before it changes live data.

1. Confirm each page reads the expected source, fields, and records. Test empty and error states as well as a normal record.
2. Run queries and transformations with safe inputs. Inspect the request method, destination, credentials, and result of any write action.
3. Try each role: a builder, a staff member, and an end user if the app is a portal. Confirm restricted pages, actions, and records stay restricted.
4. Test workflows and agent tools with the same access expectations. For an approval, check both approval and rejection paths.
5. Record what failed, revise only that behavior, and repeat the test.

Use [Granular Permissions](../../access-and-sharing/app-and-data-permissions/user-and-team-properties.md) for detailed rules and [Audit logs](../../access-and-sharing/audit-logs-privacy-and-security/audit-logs.md) to inspect relevant activity. Continue with [Preview and publish an AI app](preview-and-publish-an-ai-app.md).
