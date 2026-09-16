---
icon: code
---

# Functions

A function defines the steps or code you want to run. Choose how to build it first, then attach triggers to turn it into an automation.

## Choose how to build a function

In the project's Workflows area, open **Add Function** and choose one of the two options:

| Option                         | Use it when                                                                             |
| ------------------------------ | --------------------------------------------------------------------------------------- |
| **Workflow Builder** — no-code | You want to drag nodes onto a canvas, connect steps, and see the workflow visually.     |
| **Write Code** — TypeScript    | You want to implement the logic in code and import JavaScript dependencies when needed. |

<figure><img src="../.gitbook/assets/add-function.png" alt="Add Function dialog with Workflow Builder and Write Code options"><figcaption><p>Choose a visual workflow or TypeScript code. Attach triggers later to turn the function into an automation.</p></figcaption></figure>

## Build visually

1. Select **Workflow Builder**.
2. Add the steps your process needs and connect them on the canvas.
3. Configure the data passed between steps.
4. Test the logic with representative inputs before attaching a trigger.

For individual concepts, see [Add and configure actions](build-workflow-steps/add-and-configure-actions/), [Pass inputs into a workflow](build-workflow-steps/pass-inputs-into-a-workflow.md), and [Add conditions and branches](build-workflow-steps/add-conditions-and-branches.md).

## Write code

Select **Write Code** to implement the function in TypeScript. This option also supports importing JavaScript dependencies.

Use the editor's generated structure and available controls when configuring your function. Check the inputs your code expects, the result it returns, and how it handles missing or invalid values.

Choose this option when expressing the logic in code is more practical than arranging visual steps. The creation dialog selects the authoring method; it does not itself configure a trigger.

## Attach a trigger

After building the function, attach the trigger that should start it. See [Start a workflow](start-a-workflow/) for the trigger concepts and guides.

The component **Run Workflow** controls described elsewhere in this section are a separate entry point. Use the controls shown in your current editor rather than assuming a component's Actions configuration is part of the Add Function dialog.

## Test the result

Check a normal input, an empty or missing value, and a failure case. Inspect the resulting data as well as the returned output. Tests that perform writes or external actions can have real effects.

See [Test steps and complete workflows](test-and-troubleshoot/test-steps-and-complete-workflows.md).

These workflow functions are different from the formula functions used in computed fields. For formula syntax, see [List of Functions](../user-guide/data/computed-fields/formulas/list-of-functions.md).
