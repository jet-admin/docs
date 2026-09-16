---
description: In this section you will learn about triggers
---

# Choose a trigger

A trigger determines when a process starts and what information it receives.

| Starting event                        | Use                    | Input to define                                          |
| ------------------------------------- | ---------------------- | -------------------------------------------------------- |
| A user clicks a button                | Component workflow     | Selected record ID or form values                        |
| A user runs a list action             | Component workflow     | The row or selected-record values exposed by that action |
| A component action succeeds or fails  | Success/error callback | Values available in the component's action context       |
| A regular interval                    | Scheduled automation   | Query criteria and timing                                |
| Another service sends an HTTP request | Webhook automation     | Event payload and record identifier                      |

## Component or background automation?

For a component workflow, open the component's **Actions** configuration and choose **Run Workflow**. Follow [Run from a button or list action](run-from-a-button-or-list-action.md).

For unattended work, open **Automation** and use a [schedule](run-on-a-schedule.md) or [webhook](receive-an-incoming-webhook.md). Read records explicitly instead of relying on an open app page.

Success/error callbacks belong to component action configuration. They are distinct from conditions inside a workflow; see [Run actions after component success or failure](../handle-outcomes/component-success-and-failure-actions.md).

## Check the input

Before adding actions, identify one value that the process must receive, such as `ticket_id`. Define its type, supply a test value, and inspect it at the first step. See [Pass inputs into a workflow](../build-workflow-steps/pass-inputs-into-a-workflow.md).
