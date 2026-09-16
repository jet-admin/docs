---
icon: rocket
---

# Publish your app

Publish after the reviewed app, data connections, and permissions match the intended use.

## Before publishing

* Confirm the target [environment](../environments/) and resources.
* Complete [data and access tests](../../ai-app-builder/test-and-publish/check-data-actions-and-user-access.md) with synthetic records.
* Check [Desktop, Tablet, and Mobile](../../ai-app-builder/preview-and-troubleshoot/control-app-preview.md) layouts.
* [Preview as an invited user](../../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) and resolve relevant errors.
* Record the reviewed [app version](../../ai-app-builder/test-and-publish/version-history.md) and recovery approach.

## Publish the reviewed changes

1. Open the intended app and environment.
2. Review the result of the last generated or manual change.
3. Select **Publish** in the top toolbar.
4. Follow any publishing options or confirmation shown for your app.
5. Open the published app at its configured address.
6. [Verify the release](verify-a-release.md) with an intended test user.

![Builder toolbar with separate Share, Version History, and Publish controls](../../.gitbook/assets/publish-toolbar.png)

Non-builder users see the published app. A change that appears in Preview may still be unpublished.

For the AI builder's full walkthrough, see [Preview and publish an AI app](../../ai-app-builder/test-and-publish/preview-and-publish-an-ai-app.md). For an existing Classic app, see [Classic Preview & Publish](../../classic-app-builder/preview-and-publish/).

## If the result differs from Preview

Start with [Published changes are missing](../logs-and-troubleshooting/published-changes-missing.md). Check the environment, address, and publication result before making another app change. Publishing and inviting a user are separate actions; use [Share with the intended audience](../share-and-embed/share-your-app.md) when access is the next step.
