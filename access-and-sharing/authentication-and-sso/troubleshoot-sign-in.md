# Troubleshoot sign-in

Separate authentication failures from permission and publishing problems before changing settings.

## Check the symptom

| Symptom                                  | Check first                                                                                   |
| ---------------------------------------- | --------------------------------------------------------------------------------------------- |
| Invitation cannot be found               | Recipient email, spam or quarantine, and the intended app.                                    |
| Login returns to the sign-in screen      | Provider configuration, current callback or redirect values, and provider-side error details. |
| Sign-in works but the app is unavailable | Membership, team assignment, app environment, and published version.                          |
| The wrong pages or records appear        | [App and data permissions](../app-and-data-permissions/) and user properties.                 |
| Builder and user see different versions  | Whether the intended app changes are published.                                               |

## Collect a useful reproduction

1. Record the app, environment, sign-in method, time, and visible error.
2. Reproduce with a separate intended test account.
3. Open **More → System logs** and filter around that time.
4. Compare the app's authentication settings with the provider configuration.
5. Retest the same account after one configuration change at a time.

[System logs](../audit-logs-privacy-and-security/investigate-system-logs.md) may help explain authentication and integration errors. An empty result does not establish that sign-in succeeded or that no error occurred.

Keep passwords, tokens, cookies, and client secrets out of screenshots and shared error reports. Include the symptom and relevant redacted details instead.

Before disabling an existing method, verify that another administrator sign-in path works.
