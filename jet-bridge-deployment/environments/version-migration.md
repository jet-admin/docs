---
description: Select a Jet Admin platform version and test updates before Production.
---

# Update to a new version

Use the **Jet Admin Version** selector in environment settings to control platform updates. This is separate from [Version History](../../ai-app-builder/test-and-publish/version-history.md), which tracks changes to your app.

## Update through environment settings

1. Open the app menu in the top-left corner of the builder.
2. Under **Environments**, select the gear icon beside the environment you want to update.
3. Review **View Changelog**.
4. Select **Latest** for automatic platform updates, or choose a specific available version.
5. Select **Save**.
6. Verify the selected setting and test your app's important flows.

See [Environments](./) for the current settings screen and the staging-to-production scenario. The version number displayed beside Latest changes over time.

## Test before updating Production

Start in a staging environment connected to appropriate test resources. Check pages, data actions, integrations, workflows, and user permissions. Record the tested platform version before selecting it in Production.

Download an environment backup before a significant update. For major-version changes, review compatibility requirements and confirm your recovery approach before applying changes. A configuration created or saved on a newer platform version may not work on an older one; do not assume that selecting an older version is a complete rollback.

## Earlier migration reference

The notes below apply specifically to the historical 1.x.x-to-2.x.x transition. They do not describe current platform limitations.

## Historical migration: 1.x.x to 2.x.x

What should be done before the update:

* If you have never saved Menu items – apply any change and save menu customization

What should be done after the update:

* If you use any 3rd party integrations – run the Sync operation inside the resource settings

The following functionality is temporarily unavailable in 2.x.x:

* Adding/displaying Custom Fields (ex. FlexFields)
* Adding Collection segments in the Menu
* Adding Custom Views (ex. FlexViews)
* Adding Webhook tasks

The following features will be deprecated in the future and should be reconfigured differently

* Dashboard page type (use Custom page instead)
* Collection Segments (use Menu items grouping instead)
