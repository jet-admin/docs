# Control page and action access

Define what each audience can open and do before configuring the app.

## Write an access matrix

For a ticket app, start with an example like this and adapt it to your requirements:

| Audience      | Ticket list               | Update tickets            | Delete tickets            | Build the app |
| ------------- | ------------------------- | ------------------------- | ------------------------- | ------------- |
| Reviewer      | Allowed                   | Denied                    | Denied                    | Denied        |
| Support agent | Allowed                   | Allowed within scope      | Denied                    | Denied        |
| App builder   | According to admin policy | According to admin policy | According to admin policy | Allowed       |

This is a design example, not a claim about automatic defaults.

## Implement the rules

Apply the app's available page, component, and action controls for each team. In AI-generated apps, inspect the resulting implementation and the authorization applied to data requests. In Classic apps, use the page and conditional-action settings available in that builder.

See [Classic conditional add, edit, and delete](../../classic-app-builder/design-and-structure/components-visibility/conditional-add-edit-and-delete.md) and [Classic component visibility](../../classic-app-builder/design-and-structure/components-visibility/conditional-visibility/) for those specific interfaces.

## Verify the result

Use [invited-user preview](../../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) to inspect navigation and controls. Then test with the intended account:

* Open an allowed page.
* Attempt to open a restricted page directly.
* Run an allowed action against a test record.
* Attempt a denied action and verify the record did not change.

Include workflow actions and API requests used by the page. Continue with [record access](record-access.md) so a permitted action cannot affect another user's records.
