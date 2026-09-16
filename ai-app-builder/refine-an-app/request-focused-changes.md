# Request focused changes

Describe one observable change, identify its target, and say what should stay the same.

## Request a revision

1. Return to the chat for the task.
2. Name the page and component or action.
3. State the expected behavior using actual field names.
4. Send the request and wait for it to finish.
5. Test the changed behavior and a nearby behavior that should be unchanged.

> On the Tickets page, add a Status filter above the table. Keep the existing columns and sort order. Choosing Open should show only records where Status is Open.

Other examples:

* “In the ticket detail view, show Assigned to below Priority.”
* “Require a rejection reason on the approval form. Keep the existing approval permissions.”
* “On mobile, keep the New ticket button visible without horizontal scrolling.”

For a visual target, [select the component in Preview](edit-components-in-preview.md) and enter the change there.

## If the revision is too broad

Identify the unintended change and request a correction to that specific behavior. Compare the result with your last working checks before continuing.

Use [Console and logs](../preview-and-troubleshoot/inspect-app-console-and-logs.md) for an error and [the review checklist](review-and-refine.md) for behavior that looks plausible but is wrong.
