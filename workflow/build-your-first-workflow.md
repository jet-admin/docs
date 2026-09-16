---
icon: rocket
---

# Build your first workflow

Create a button workflow that changes one ticket's status. You will pass the selected ticket's ID into the workflow, configure an update action, and check the saved record.

## Before you start

You need a Tickets table, a table component displaying its records, a button, and permission to update a test record. The example uses `id` and `status`; use the actual field names in your data source. Choose an existing status value such as `In progress`, or add that choice if you own the test table.

Use a fictional ticket and note its original status. Testing an update action can change connected data.

## 1. Open the workflow builder

1. Select the button in the app builder.
2. Open its Actions configuration and select **Click action**.
3. Choose **Run Workflow** to open or select the component's workflow.

{% @arcade/embed url="https://app.arcade.software/share/2dlzfHAvIKSulhTj03j5" flowId="2dlzfHAvIKSulhTj03j5" %}

## 2. Pass the selected ticket ID

1. Select the trigger step and add a parameter named `ticket_id`. Match its type to the source ID.
2. Give it a test value that identifies your fictional ticket.
3. Return to the button action configuration. Bind the workflow input to the selected row's ID using the value picker.
4. Return to the workflow. Use the parameter as the update action's record ID.

The test value helps configure the workflow; the button still needs a runtime input binding. See [Pass inputs into a workflow](build-workflow-steps/pass-inputs-into-a-workflow.md).

## 3. Add the update action

1. Click **+** and add a data action.
2. Choose the resource and Tickets collection.
3. Choose its update operation.
4. Set the record ID from `ticket_id` and set the status to your chosen value.

![](../.gitbook/assets/etjzhcr.png)

The illustration shows the resource, collection, and action controls. Choose your own Tickets resource rather than copying the pictured resource name.

## 4. Test and check the result

1. Test the update step with your known ticket ID.
2. Inspect its output or error in the test panel.
3. Open the record in the Data Editor and verify the stored status.
4. Select the same ticket in your app and run the button workflow.
5. Check that the selected ticket changed and another ticket did not.

A successful editor test alone does not prove the button input is bound correctly. Test both routes.

## If it does not work

* **No record changed:** compare the input ID with the source record, including its type.
* **The wrong record changed:** check the selected-row binding and remove a hard-coded record ID.
* **The update failed:** check write access and whether the status is an allowed value.

Restore the original test status when finished. Next, [add a condition](build-workflow-steps/add-conditions-and-branches.md) or [use the step result](build-workflow-steps/use-step-outputs-and-return-results.md).
