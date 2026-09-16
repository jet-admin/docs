---
description: Automate business processes with triggers, actions, and rules.
icon: compass
---

# Overview: workflows and automations

Use a workflow to run defined steps: read data, check a condition, update a record, and show the result. Start with [Build your first workflow](build-your-first-workflow.md) to pass a ticket ID from a button into an update action.

## Choose where the process starts

| You want to…                                                     | Start here                                                                                                 | Configure it in                       |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| Run steps when an app user clicks a button or uses a list action | [Button and list actions](start-a-workflow/run-from-a-button-or-list-action.md)                            | The component's Actions configuration |
| Run work at a regular interval                                   | [Scheduled automation](start-a-workflow/run-on-a-schedule.md)                                              | Automation                            |
| Respond to an HTTP event from another service                    | [Incoming webhook](start-a-workflow/receive-an-incoming-webhook.md)                                        | Automation                            |
| Require a person to approve an action                            | [Approval process](practical-guides/create-an-approval-process.md)                                         | The button's approval configuration   |
| Generate workflow steps from a description                       | [Generate with AI](workflows-and-ai/generate-a-workflow-with-ai.md)                                        | Ask AI in the workflow builder        |
| Let an agent interpret input during a run                        | [Run an agent in a workflow](../ai-agents/run-agents-in-apps-workflows-and-tasks/workflows-with-agents.md) | An agent step within the workflow     |

Component workflows can use values from the app. Background automations need their own trigger inputs or data queries; do not assume a selected row or visible component is available.

## Learn in order

1. [Build and test a first workflow](build-your-first-workflow.md).
2. [Pass inputs](build-workflow-steps/pass-inputs-into-a-workflow.md) and [use step outputs](build-workflow-steps/use-step-outputs-and-return-results.md).
3. Add [conditions](build-workflow-steps/add-conditions-and-branches.md) or an [iterator](build-workflow-steps/process-multiple-records-with-iterators.md).
4. [Test the normal, empty, and failure cases](test-and-troubleshoot/test-steps-and-complete-workflows.md).
5. Use [troubleshooting](test-and-troubleshoot/troubleshoot-common-problems.md) when a step does not produce the expected result.

The examples use fictional Tickets records. Use your own field names and allowed status values when adapting them. Guides that show component Actions, list actions, or task queues apply to the builder interface containing those controls.
