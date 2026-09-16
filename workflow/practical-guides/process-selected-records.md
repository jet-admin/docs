# Process selected records

Pass an explicit list of record IDs into an iterator when an app user chooses which tickets to process.

## Before you start

You need a component action that exposes the selected records or their IDs, plus permission to update the test tickets. Inspect the values available in that action. A filtered list is not necessarily an explicit selection.

## Configure the workflow

1. Select two fictional tickets.
2. Configure the component action to run a workflow.
3. Add an input parameter named `ticket_ids` for an array of IDs, matching the type offered by the builder.
4. Bind the component's selected IDs to that parameter. If the component provides record objects, use its supported value-mapping controls to extract IDs, or pass the objects and reference each current item's ID.
5. Add an iterator with **Specify Iterate** and bind the array.
6. Add the update action inside the iterator.
7. Bind its record ID to the current item, or the current item's ID for an array of objects.

For example, an ID-array test input might be `[1, 2]`. A record-object input has a different shape; inspect it before mapping.

## Verify the selection

Check that the two selected tickets changed and an unselected ticket did not. Then test an empty selection. No ticket should be updated when the array is empty.

If the component does not expose selected records, do not substitute all visible rows. Use an explicit ID input or follow the separate [filtered-collection iterator pattern](../build-workflow-steps/process-multiple-records-with-iterators.md) and label the action accordingly.

## Check failures

If processing stops after some records change, inspect which IDs completed before running it again. See [partial success and duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).
