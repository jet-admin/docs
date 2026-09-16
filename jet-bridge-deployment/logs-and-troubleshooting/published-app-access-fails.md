# Published app access fails

Determine whether the failure happens before sign-in, during authentication, or after the user's identity is established.

## Check the symptom

| Symptom                                               | Investigate                                                                                                                   |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Address does not load                                 | [Domain configuration](../custom-domains/troubleshoot-a-domain.md) or [deployment health](resource-and-deployment-errors.md). |
| Invitation is missing or unusable                     | Email, intended app, and [invitation workflow](../../access-and-sharing/members-users-and-groups/invite-by-email.md).         |
| Sign-in loops or returns an error                     | [Authentication troubleshooting](../../access-and-sharing/authentication-and-sso/troubleshoot-sign-in.md).                    |
| Sign-in succeeds but pages or actions are unavailable | Membership, team, and [permissions](../../access-and-sharing/app-and-data-permissions/).                                      |
| App works directly but not embedded                   | Host support and [embedded authentication behavior](../share-and-embed/embed-an-app.md).                                      |

## Reproduce with the intended account

Confirm the exact published address, environment, and signed-in identity. Review the user's membership and all relevant team assignments, then compare the behavior with the intended access policy.

Do not grant Administrator access simply to make a failed user test pass. Correct the specific identity, membership, or permission issue.

Inspect available [system logs](../../access-and-sharing/audit-logs-privacy-and-security/investigate-system-logs.md) around the failure time. For custom domains, check any identity-provider settings that depend on the address.

After a correction, run both allowed and denied cases from [the access test checklist](../../access-and-sharing/overview/test-access.md). Verify the published app, not only the builder preview.
