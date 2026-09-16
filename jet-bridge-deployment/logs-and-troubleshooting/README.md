---
icon: wrench
---

# Troubleshooting

Start with the symptom, then inspect the part of the release path responsible for it.

| Symptom                                          | Guide                                                                        |
| ------------------------------------------------ | ---------------------------------------------------------------------------- |
| Preview has a change that users cannot see       | [Published changes are missing](published-changes-missing.md)                |
| User cannot sign in or sees the wrong access     | [Published app access fails](published-app-access-fails.md)                  |
| Custom address does not load correctly           | [Troubleshoot a custom domain](../custom-domains/troubleshoot-a-domain.md)   |
| Data, actions, or self-hosted services fail      | [Diagnose resource and deployment errors](resource-and-deployment-errors.md) |
| App works directly but fails inside another site | [Embed an app](../share-and-embed/embed-an-app.md)                           |

## Collect a reproducible report

Record the app, environment, exact address, affected role, action, time with timezone, expected result, and actual result. Include the relevant app version and platform version when known.

Use [System logs](../../access-and-sharing/audit-logs-privacy-and-security/investigate-system-logs.md) for available diagnostic messages and [the audit trail](../../access-and-sharing/audit-logs-privacy-and-security/review-the-audit-trail.md) for available activity. Remove credentials and unnecessary personal data from shared evidence.

## Choose the right next step

Compare the problem with the last working configuration. Make one targeted correction, then repeat the same failed check.

If recovery is needed, choose between [app version history](../../ai-app-builder/test-and-publish/version-history.md), [environment restoration](../environments/), and the affected data system's recovery process. These have different scopes.

For AI generation or revision failures, use [AI App Builder troubleshooting](../../ai-app-builder/preview-and-troubleshoot/troubleshoot-the-prompt-assistant.md).
