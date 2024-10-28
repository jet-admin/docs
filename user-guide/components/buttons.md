---
description: Buttons overview
---

# Buttons

Buttons are the execution of any action. For example, you can create buttons to execute: Copy to clipboard, Send an email, Open a link, Link to page and others.

### Adding button

To add a button, you need to go to Visual Builder and simply drag and drop the Action to the page, specify the button name and action type. More information about types of [Actions](../design-and-structure/actions.md).

![](<../../.gitbook/assets/GIF (237).gif>)

### Send an email button

For example, you want to add a button that will send emails. To do this, select the type of Action - **Run Operation**, and then configure the action to send an email (example below: using Sendgrid to do this). For more details about how to set up Actions, see [here.](https://docs.jetadmin.io/user-guide/design-and-structure/actions)

![](<../../.gitbook/assets/GIF (236).gif>)

### Confirmation Dialog

The Confirmation Dialog is ideal for scenarios where user confirmation is necessary before proceeding with critical operations, such as deleting a record, submitting a form, or making significant changes. By asking users to confirm their intentions.

<figure><img src="../../.gitbook/assets/Screenshot 2024-06-08 011533.png" alt="" width="201"><figcaption></figcaption></figure>

#### Customization

Title and Description

You can customize the dialog's title and description to provide clear and relevant information to the user. This ensures that users understand the action they are about to confirm.

Buttons

The dialog includes two customizable buttons:

1. **Submit Button**: The button used to confirm the action. You can set its name, color, and icon.
2. **Cancel Button**: The button used to cancel the action. You can also set its name, color, and icon.

Disabling the Confirmation Dialog

To disable the confirmation dialog, simply scroll to the end of the dialog settings and click on "Disable Confirmation Dialog." This will turn off the popup and allow actions to proceed without requiring user confirmation.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Show/Hide Notification Messages

By default, notification messages show after each action's success or fail happens. This feature allows you to enable or disable these action's automatic notification messages. depending on your case.

<div align="left">

<figure><img src="../../.gitbook/assets/image (948).png" alt=""><figcaption></figcaption></figure>

</div>

Using this feature, you can create custom notifications after each success or fail. \
To achieve this, first you need to disable the default notification and create a new action in the 'WHEN ACTION SUCCEEDED' or 'WHEN ACTION FAILED' section. Then set this new action to show a customized notification message.

![](<../../.gitbook/assets/image (949).png>)&#x20;



More information about Actions.

{% content-ref url="../design-and-structure/actions.md" %}
[actions.md](../design-and-structure/actions.md)
{% endcontent-ref %}
