---
description: Add actions that users can trigger
---

# Run Actions

A helpful way to think about apps is through how users interact. Two elementary levels of interaction are viewing and editing data, which we built on the previous steps. But often, apps need to be able to perform custom actions with specific workflow.

Initiating a **Form** is a form of action. Actions such as **Open Link** and **Show notification** are native functionalities within Jet, triggering specific processes within your app.

In this tutorial, we'll set up a system to automatically send notifications to the user via email and Slack when a deal is marked as **Closed Won**.

1. Initiate the workflow when the **Deal** is updated, which occurs when the associated form is successfully submitted.

{% @arcade/embed flowId="xwy9H9O3HZpT5S9hShmp" url="https://app.arcade.software/share/xwy9H9O3HZpT5S9hShmp" %}

2. Add a conditional step in the workflow that checks whether the deal stage is set to **Closed Won.** For the conditional step, employ the 'Equals' operation using the [Formula](../../user-guide/formulas.md) `EQ({deal_stage}, 'Closed Won')` to verify if the deal stage matches the **Closed Won** status. The value for {deal\_stage} is selected from Formula.

{% @arcade/embed flowId="0oY95MDbyTrkHCRLTqzX" url="https://app.arcade.software/share/0oY95MDbyTrkHCRLTqzX" fullWidth="false" %}

3. **Send email**. Add actions to send an email with the content formatted as: `"Deal {0} is Closed Won"`. Here, `{deal_name}` should be dynamically inserted into the email content, and its value can be selected using a formula that references the `{deal_name}` field from the data source.

{% @arcade/embed flowId="i1idRrbrtOyTqGYgPNFK" url="https://app.arcade.software/share/i1idRrbrtOyTqGYgPNFK" %}

4. **Show notifications**. Use the same logic to implement notifications.

{% @arcade/embed flowId="efqZNcKZhvcZqqyfucne" url="https://app.arcade.software/share/efqZNcKZhvcZqqyfucne" %}
