# Build a support dashboard

Create a workspace for finding, reviewing, and assigning support tickets.

## Prepare data

Use a Tickets table with Name, Status, Priority, Assigned to, and Customer fields. Connect Customers for customer details. Confirm how Customer links to its record. Include two Open test tickets and one Closed test ticket.

For starter ticket records, [download the sample CSV](../../.gitbook/assets/sample-tickets.csv). Add a Customer relationship and sample customer records separately for the customer-detail steps.

## Build the list and details

1. [Select the source](../ai-assistant/select-data-sources.md) containing the tables.
2. Send this prompt, replacing field names as needed:

> Build a support dashboard using Tickets and Customers. Show Name, Status, Priority, and Assigned to in a Tickets list. Add search by Name and a Status filter. Open a detail view when I select a ticket and show its linked customer. Start read-only.

3. Confirm all test records appear.
4. Filter to Open: exactly the two Open test tickets should remain.
5. Open a ticket and compare its customer details with the linked source record.

## Add assignment

> Add an assignment action to the ticket detail view. Update only Assigned to on the selected ticket. Require a value and display the saved result.

Test the action on one ticket. Verify the source record changed and the other tickets did not. Configure and test the permissions for staff who may assign tickets.

## Refine and release

Use [Edit in Preview](../refine-an-app/edit-components-in-preview.md) for a label change and [Theme](../themes-and-appearance/) for appearance. Check mobile navigation and form layout.

Finish with [data and access testing](../test-and-publish/check-data-actions-and-user-access.md) and [publishing checks](../test-and-publish/preview-and-publish-an-ai-app.md). If a source update fails, capture its inputs and error in [Console](../preview-and-troubleshoot/inspect-app-console-and-logs.md).
