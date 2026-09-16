---
icon: code-branch
---

# Environments, releases, and version control

Keep testing separate from the app people use. [Environments](environments/) explains how to manage stages, and [Version Control](version-control/) covers tracked changes and recovery.

Before a release, confirm the data connection, user roles, and actions in the target environment. Check any generated query or workflow that writes records. Record which version was approved and how to restore a previous working state. For platform upgrades, see [Update to a new version](version-migration.md).

## Review app versions

Use [Version History](../../ai-app-builder/test-and-publish/version-history.md) in the AI App Builder to browse dated changes, preview a version, inspect its changes, and choose a version to revert to. Verify the app after reverting and complete your publishing checks before release.
