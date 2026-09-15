---
description: In this section you will learn how to update to a new version
---

# Update to a new version

An update to a new major version can lead to some settings not being saved and there is a chance you won't be able to go back to the previous version after saving changes to the interface because of breaking changes. So do it carefully and at your own risk.&#x20;

**It is safe to create a separate project for the new version and copy settings from the old project. We highly recommend this way so you will able to revert any time.**

We are always trying to make version updates fully compatible so you don't need to make anything on your own, but there could be a few that can't be done automatically.&#x20;

**You can check your current Jet Admin version in Project Settings**

![](<../../.gitbook/assets/image (857).png>)

## Migrating from 1.x.x to 2.x.x

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
