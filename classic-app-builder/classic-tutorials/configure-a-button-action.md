---
icon: hand-pointer
---

# Configure a button action

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Run a resource operation from a button and verify its effect.

**Before you start:** choose a test operation, identify its required inputs, and prepare synthetic data.

## Configure the action

1. Add or select a **Button** component.
2. Open **Click Action**.
3. Choose **Run Operation**.
4. Choose the **Resource** and **Action**.
5. Bind the required inputs, including the record identifier when the operation needs one.
6. Where appropriate, use **Confirm on execute** to explain the action before execution.
7. Preview and run the operation with the intended test account.

![Classic action settings showing the available action configuration](<../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

![Classic Confirm on execute configuration](<../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

## Verify the result

Check the actual source record or operation result. Test missing inputs and a restricted user. If a confirmation is configured, cancel it and confirm that the operation does not run.

For navigation, choose **Navigate to Page** instead and pass the required page parameters. For a sequence, use the relevant workflow action.

See [Actions](../actions-and-logic/actions.md) for the full reference.

## Existing Classic walkthrough

{% @arcade/embed url="https://app.arcade.software/share/hiEUE1MH878JTe5ffe6h" flowId="hiEUE1MH878JTe5ffe6h" %}
