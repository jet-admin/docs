# Preview and publish an AI app

Publish the app after checking its pages, data actions, and user access.

## Before publishing

Complete [data and access tests](check-data-actions-and-user-access.md). Inspect [Desktop, Tablet, and Mobile](../preview-and-troubleshoot/control-app-preview.md) and confirm the app works for an invited user. Resolve relevant Console errors.

## Publish

1. Open the project and environment you intend to release.
2. Review the app after the last generated or manual change.
3. Click **Publish** in the builder's top toolbar.
4. Review the publishing options shown for your project and complete the publish flow.
5. Open the published app at its configured address.

For environment configuration, domains, and deployment choices, follow [Publish & Deploy](../../jet-bridge-deployment/overview/).

## Check the published app

Sign in as a representative user. Open the critical pages and repeat the main task with test records. Verify the source result of a write action and check a restricted user is still denied.

A successful Preview check is useful evidence, but the published app must also be checked with its actual configuration.

## If publication or verification fails

Capture the error, environment, app URL, and time. Determine whether the problem is publishing, loading, data access, or an action before changing the app.

Use [Console and logs](../preview-and-troubleshoot/inspect-app-console-and-logs.md) for Preview diagnostics and [troubleshooting](../preview-and-troubleshoot/troubleshoot-the-prompt-assistant.md) for a failed generation or revision.
