# Review generated pages and logic

Treat the generated app as a draft to check against the job you described.

## Review a page

1. [Open the page in Preview](select-a-page.md).
2. Compare its labels and fields with the source schema.
3. Match one displayed record to the source record.
4. Test filters, search, sorting, and detail navigation.
5. Test an empty result and a record with missing optional fields.

## Review actions and logic

For an action, identify its inputs, destination, and expected result. Inspect any generated query, API call, workflow, or transformation before testing a write.

For example, an assignment action should update the selected ticket's Assigned to field, not every ticket or an unrelated field.

## Record the result

| Check                          | Expected result                              |
| ------------------------------ | -------------------------------------------- |
| Status filter set to Open      | Only Open tickets appear.                    |
| Search for a ticket name       | The matching ticket remains.                 |
| Open ticket details            | The values match the selected source record. |
| Restricted user opens the page | Access matches the configured rules.         |

Use [a focused change request](request-focused-changes.md) for each failed check. Repeat the check after the revision.

Next: [Test data actions and user access](../test-and-publish/check-data-actions-and-user-access.md).
