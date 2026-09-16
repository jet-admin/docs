# Write your first prompt

A useful prompt names the users, connected data, screens, and allowed actions. Start with an outcome you can verify against a few records.

## Build the prompt

| Include       | Example                                     |
| ------------- | ------------------------------------------- |
| Users and job | Support staff reviewing incoming tickets    |
| Data source   | Tickets in the selected Jet Tables resource |
| Fields        | Name, Status, Priority, Assigned to         |
| Screens       | Ticket list and a detail view               |
| Behavior      | Filter by Status; search by Name            |
| Scope         | Read-only first version                     |

> Build a support app for staff using Tickets from the selected resource. Show Name, Status, Priority, and Assigned to in a searchable list. Add a Status filter and a detail view for a selected ticket. Use connected records and start with a read-only version.

## Send and review

1. [Select the data source](../ai-assistant/select-data-sources.md).
2. Enter the prompt by [typing or dictating](../ai-assistant/type-or-dictate-a-prompt.md).
3. Add [an image or file](../ai-assistant/upload-images-and-files.md) only when it helps explain the requirement.
4. Send the request and answer any clarification questions.
5. Compare the generated result with the fields and behavior you requested.

## Improve a vague request

Instead of “Make it better,” identify the observable change:

> On the Tickets page, place Priority beside Status and sort Open tickets first.

A prompt requesting a permission rule is a requirement to verify. It does not prove the generated app enforces that rule.

Next: [Review generated pages and logic](../refine-an-app/review-and-refine.md).
