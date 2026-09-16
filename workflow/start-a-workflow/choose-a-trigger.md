---
description: In this section you will learn about triggers
---

# Choose a trigger

A trigger defines when a function runs automatically. In the **Workflows** area, choose **Add Automation** to start with a trigger, or use **Add trigger** for an existing function.

## Function and automation triggers

| Trigger                  | Starts work                         |
| ------------------------ | ----------------------------------- |
| **At regular intervals** | Repeatedly at a configured interval |
| **Based on a schedule**  | According to a configured schedule  |
| **One-time run**         | For a single configured execution   |
| **When record created**  | When a new record is created        |
| **When record updated**  | When a record is updated            |
| **When record deleted**  | When a record is deleted            |

Follow [Functions and automations](../functions.md) for screenshots of both menus and the setup sequence. Configure the timing or record source after choosing a type.

## Component actions

An app user can also start a workflow from a button or list action. Open the component's **Actions** configuration and choose **Run Workflow**. Bind the selected record ID or form values as inputs.

See [Run from a button or list action](run-from-a-button-or-list-action.md). Component success/error callbacks are another entry point; see [Run actions after component success or failure](../handle-outcomes/component-success-and-failure-actions.md).

## External HTTP events

The separately documented [webhook setup](receive-an-incoming-webhook.md) covers incoming HTTP events. A webhook option is not shown among the six choices in the supplied Add trigger and Add Automation menus.

## Check the input and result

Identify the values the function needs, inspect the inputs supplied by the trigger, and map the required fields. A record event and an app's selected row may expose different data.

Test both the function and its actual trigger. For update events, check whether the function's writes can cause another event. For deletion events, inspect the payload rather than assuming the deleted record remains queryable.

See [Pass inputs into a workflow](../build-workflow-steps/pass-inputs-into-a-workflow.md) and [Handle failures and prevent duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).
