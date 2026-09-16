---
description: In this section you will learn about Iterators
---

# Process multiple records with iterators

An iterator runs its nested steps for each item in a collection or array. Use it to process several tickets with the same action.

## Choose the input mode

| Mode                | Use it when                                             | Configure                         |
| ------------------- | ------------------------------------------------------- | --------------------------------- |
| **Load Data**       | The iterator should query a connected collection        | Resource, collection, and filters |
| **Specify Iterate** | A previous step or parameter already contains the items | The array to iterate              |

<figure><img src="../../.gitbook/assets/image (941).png" alt=""><figcaption><p>Iterator settings</p></figcaption></figure>

A filtered collection and a user's explicitly selected records are different inputs. For selection-based processing, see [Process selected records](../practical-guides/process-selected-records.md).

## Add the iterator

1. Open the component workflow, or open **Automation** and add an automation.
2. Configure the trigger.
3. Add an iterator and select its input mode.
4. Add the repeated actions inside it. You can also move existing steps into the iterator.
5. Bind each action to the current item's fields.

{% @arcade/embed url="https://app.arcade.software/share/QP5qx9WJgYAGSaSnoQix" flowId="QP5qx9WJgYAGSaSnoQix" %}

For a ticket update, use the current item's ID. Binding every iteration to a single trigger ID would repeatedly target the same ticket.

## Example: process a filtered collection

The existing walkthrough uses customers filtered by city. Apply the same pattern to Tickets filtered by priority or status.

<figure><img src="../../.gitbook/assets/image (940).png" alt=""><figcaption><p>A table with customers, multiple-select filter and button with a workflow action</p></figcaption></figure>

1. Display records in a table and configure the filter component.
2. Pass the filter value into a workflow parameter.
3. Choose **Load Data** and configure the same filter for the iterator's collection query.
4. Add a temporary in-app notification to inspect the current item in a component workflow.
5. After checking the selected scope, configure the intended action.

{% @arcade/embed url="https://app.arcade.software/share/S6oREqJWf6Dzv91I9xVD" flowId="S6oREqJWf6Dzv91I9xVD" %}

{% @arcade/embed url="https://app.arcade.software/share/CyuvyHn4OULwyYZZKc0o" flowId="CyuvyHn4OULwyYZZKc0o" %}

The iterator's query must include the filter; do not assume it automatically inherits a table component's filter.

## Test before processing the full list

Start with two fictional records and confirm each is processed once. Test an empty array or a filter returning no rows. Inspect the current item binding and final records. The existing email walkthrough should be tested only with recipients you control.

For actions that can be repeated or partially fail, see [failure handling and duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).
