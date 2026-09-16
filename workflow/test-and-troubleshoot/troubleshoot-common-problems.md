# Troubleshoot common problems

Start with the failing step, the input it received, and the data that changed.

| Symptom                                     | Check                                              | Next action                                                   |
| ------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------- |
| Works in the editor but not from the button | Runtime input binding and selected record          | Bind the input to the component value, then test from the app |
| Wrong record changes                        | ID field, hard-coded values, current iterator item | Compare the exact target ID with the intended record          |
| A condition takes the wrong route           | Type, spelling, capitalization, blank values       | Inspect the input and test both branches                      |
| A later action has no result to use         | Whether the earlier step ran and its output shape  | Bind the required field and handle an empty result            |
| Iterator updates the same record repeatedly | Current-item binding                               | Use each current item's ID instead of one fixed trigger ID    |
| Iterator processes too many records         | Query filters or selected-record input             | Distinguish filtered rows from explicit selection             |
| Schedule does not run as expected           | Enabled state, interval, effective time zone       | Verify a controlled scheduled execution                       |
| Webhook does nothing                        | Sender request result, URL, method, format         | Send a sample matching the trigger configuration              |
| Repeated event sends another notification   | Event tracking and partial success                 | Follow the duplicate-processing pattern                       |
| Approval request exists but action failed   | Operation input and access                         | Inspect the action result and test with the intended accounts |
| Dependent callbacks run in the wrong order  | Parallel component success/error actions           | Move dependencies into an explicitly ordered workflow         |

## Collect useful details

Record the trigger type, expected result, received input shape, failing step, exact error, and effects already observed. Remove credentials and sensitive record values before sharing examples.

For editor controls, see [Test steps and complete workflows](test-steps-and-complete-workflows.md). For repeated or partly completed operations, see [Handle failures and prevent duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).
