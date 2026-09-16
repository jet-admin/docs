# Handle failures and prevent duplicate processing

A failed run may already have completed earlier actions. Before running it again, determine which effects occurred.

## Diagnose before retrying

1. Open the failing step and read the error in the test panel.
2. Inspect the identifier and fields passed into the step.
3. Check whether previous steps wrote records or sent notifications.
4. Correct the input, access, or configuration problem.
5. Test the affected path with a fictional record.

See [Test steps and complete workflows](../test-and-troubleshoot/test-steps-and-complete-workflows.md). Do not assume a failure rolls back earlier operations or that testing is a dry run.

## Design for repeated events

Schedules can select the same records again, and an external sender can deliver an event more than once. Choose a stable key, such as a ticket ID plus the type of reminder, or an event ID supplied by the sender.

A common application-level pattern is:

1. Look up whether that key has already been processed.
2. Skip completed work.
3. Perform the intended action.
4. Save a processed marker after success.

This is a design pattern you implement in your data and workflow, not an automatic guarantee. A lookup followed by a write can race if two runs overlap. For strict duplicate prevention, use a unique constraint or atomic operation supported by your data source.

## Account for partial success

If a message was sent but saving the processed marker failed, rerunning can send it again. Inspect the external service's result and use an idempotency key when that service supports one.

Do not assume Jet Admin or a connector retries automatically. Check the behavior of the actual trigger and operation before relying on it.

## Test the edge cases

Test the same event twice, a missing record, a denied operation, and a failure after an earlier successful step. Confirm both the displayed result and the final data.

For button feedback, configure [component success and error actions](component-success-and-failure-actions.md). For recurring work, see [scheduled reminders](../practical-guides/send-scheduled-reminders.md).
