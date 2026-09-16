---
icon: bolt
---

# Actions and logic

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Configure what happens when a user interacts with the app.

## Choose the behavior

| Need                                             | Reference                                                                          |
| ------------------------------------------------ | ---------------------------------------------------------------------------------- |
| Run a data operation or navigate                 | [Action types](actions.md)                                                         |
| Configure one button end to end                  | [Configure a button action](../classic-tutorials/configure-a-button-action.md)     |
| Store or change app state                        | [Variables](../binding-and-values/variables.md)                                    |
| Transform a value or run custom logic            | [JavaScript](javascript.md)                                                        |
| Generate a formula or JavaScript with assistance | [AI-assisted formulas and JavaScript](generate-formulas-and-javascript-with-ai.md) |
| Run a sequence of operations                     | [Run Workflow](../../workflow/overview.md)                                         |
| Refresh a component or clear a form              | [Run Component Action](../design-and-structure/components/component-actions.md)    |

## Trace the inputs and result

Before configuring an action, define its trigger, required inputs, expected output, and failure behavior. For a record update, identify both the record ID and the editable values.

Test a permitted operation on synthetic data, then a denied operation using a restricted account. A success notification is not sufficient evidence that the intended record changed.

For chained behavior, check that later actions receive the expected output and handle failures appropriately. Use [troubleshooting](../preview-and-publish/troubleshoot-a-classic-app.md) to isolate the first failing step.
