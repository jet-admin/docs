# Verify a published release

Check the released app at the address users will actually open. Passing a Preview test is useful, but does not replace this check.

**Before you start:** record the app, environment, reviewed version, published address, and release time. Prepare synthetic records and representative user accounts.

## Run the checks

| Check                                  | Expected result                                       |
| -------------------------------------- | ----------------------------------------------------- |
| Open the published address             | The intended app loads over the expected connection.  |
| Sign in as an intended user            | The correct identity and permitted pages appear.      |
| Find a known reviewed change           | The released behavior matches the approved version.   |
| Read a permitted record                | The expected data is available.                       |
| Run a permitted test write             | Only the intended source record changes.              |
| Attempt a restricted action            | The request is denied and the data remains unchanged. |
| Test a second customer or role         | No data outside that user's scope is exposed.         |
| Open the app on supported screen sizes | Navigation and essential actions remain usable.       |

## Record the outcome

For each important task, record expected result, actual result, and evidence. Include the identity and environment so another reviewer can reproduce the test.

If a check fails, identify whether it concerns [the released version](../logs-and-troubleshooting/published-changes-missing.md), [access](../logs-and-troubleshooting/published-app-access-fails.md), or [a resource or deployment service](../logs-and-troubleshooting/resource-and-deployment-errors.md). Compare with [Version History](../../ai-app-builder/test-and-publish/version-history.md) before deciding whether to correct the app or revert a change.

Repeat the affected checks after a correction or revert. Review separately whether any failed action changed data or triggered an external operation.
