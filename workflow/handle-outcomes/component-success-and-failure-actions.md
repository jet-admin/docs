---
description: In this section you will learn about Success/Error Actions
---

# Run actions after component success or failure

Use success and error actions in a component's **Actions** configuration to respond after its base action completes. For example, navigate after a form submission or show a failure response.

These are component callbacks. They do not define a global error handler for every workflow step.

## Configure a callback

1. Select the button or component.
2. Open its **Actions** tab.
3. Select **Success Action** or the error action.
4. Choose the response and configure its inputs.

![](<../../.gitbook/assets/image (865).png>)

Multiple callback operations run in parallel rather than as a guaranteed sequence. If a notification depends on an earlier update's result, put the dependent operations in an explicitly ordered workflow.

## Navigate after success

Choose **Navigate to Page** as the success action and select the destination page.

{% @arcade/embed url="https://app.arcade.software/share/3YAWw7T7y6NdF4icSGKN" flowId="3YAWw7T7y6NdF4icSGKN" %}

Test both a successful submission and a failed submission. The app should navigate only after the intended successful action.

## Send an email after success

Choose **Run Operation → App Built-ins → Send Email** and configure the recipient and message.

{% @arcade/embed url="https://app.arcade.software/share/X04eNBXIEVrUn6kV9tWv" flowId="X04eNBXIEVrUn6kV9tWv" %}

Test with an address you control. Use dynamic values from the action's available context rather than a fixed recipient intended only for setup.

## Verify failure behavior

Cause a controlled failure using fictional input. Confirm that the error response appears and that success-only effects do not occur. Check whether the base action changed any data before retrying.

See [failure handling](handle-failures-and-prevent-duplicate-processing.md) and [running a workflow from a callback](../start-a-workflow/run-from-a-button-or-list-action.md).
