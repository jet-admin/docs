---
icon: clock-rotate-left
---

# Version History

Use **Version history** to browse recorded app changes, preview a selected version, inspect its changes, or choose a version to revert to.

## Open Version History

1. Open your app in the builder and go to **Preview**.
2. Select the history icon in the top-right toolbar, beside **Publish**.
3. Review the entries in the **Version history** panel.

![Version history panel with dated entries, change descriptions, per-version menus, and the selected version marked Previewing now](../../.gitbook/assets/version-history.png)

Each entry shows a date and time, an author avatar, and a change description. The highlighted entry carries the **Previewing now** label. The selected version's information also appears above the app preview.

Use the pagination controls at the bottom to browse more entries and the refresh control to update the list.

## Preview a version

1. Find the version you want to inspect.
2. Open its **…** menu.
3. Select **Preview version**.
4. Check the **Previewing now** label to confirm which version you are inspecting.
5. Review the relevant pages and behavior in the preview.

Previewing a version and publishing an app are separate actions. Do not use the **Previewing now** label as evidence of which version your end users currently see.

## Inspect changes

Open a version's **…** menu and select **Show changes**. Review the available change details before deciding whether to return to that version.

Use the date, author, and description to identify the change you are investigating. For example, the screenshot shows an entry describing a new Tickets page and ticket-creation dialog.

## Revert to a version

1. Identify the version you intend to return to.
2. Preview it and inspect its changes.
3. Open its **…** menu and select **Revert version**.
4. Review any confirmation shown before completing the operation.
5. Check the resulting app state and repeat the affected tests.

Reverting changes the app's working state. Record the version you started from and verify the result before publishing through your normal release process. Do not assume that reverting app code or configuration restores records in a connected database or reverses workflow side effects.

After a revert, [test data actions and user access](check-data-actions-and-user-access.md), [preview as an invited user](../preview-and-troubleshoot/preview-as-an-invited-user.md), and check the published app after release.

## Use history during an access review

Record the version, environment, and test results when approving a change. If a version affects authentication, permissions, data queries, or workflows, repeat the [access test checklist](../../access-and-sharing/overview/test-access.md).

Version History helps you review app changes. Use the [audit trail](../../access-and-sharing/audit-logs-privacy-and-security/review-the-audit-trail.md) for available user activity and [system logs](../../access-and-sharing/audit-logs-privacy-and-security/investigate-system-logs.md) for diagnostic messages.

For the earlier snapshot and release interface, see [Version Control](../../jet-bridge-deployment/environments-releases-and-version-control/version-control/).
