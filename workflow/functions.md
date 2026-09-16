---
icon: code
---

# Functions and automations

Use the **Workflows** area to build the logic your app needs. Create a function with the visual Workflow Builder or write it in TypeScript, then attach triggers when it should run automatically.

## Functions and automations: what's the difference?

| Concept        | What it defines                                            | Example                                                  |
| -------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| **Function**   | The steps or code to execute, including inputs and results | Process a list and create a task for each item           |
| **Automation** | When that logic should run, through an attached trigger    | Start processing on a schedule or when a webhook arrives |

Start by building and testing the function. Configure its trigger separately when you want an automation. Component workflows started through an app's **Run Workflow** action are another entry point; their setup is covered in [Run from a button or list action](start-a-workflow/run-from-a-button-or-list-action.md).

## Create a function

Open **Add Function** and select an authoring method.

| Option                         | Use it when                                                                           |
| ------------------------------ | ------------------------------------------------------------------------------------- |
| **Workflow Builder** — no-code | You want to arrange nodes on a canvas and see the sequence and branches visually.     |
| **Write Code** — TypeScript    | You want to express the logic in code and import JavaScript dependencies when needed. |

<figure><img src="../.gitbook/assets/add-function.png" alt="Add Function dialog offering Workflow Builder and Write Code"><figcaption><p>Choose how to build the function. Attach triggers later to turn it into an automation.</p></figcaption></figure>

## Navigate the visual Workflow Builder

The visual editor shows the flow from **Workflow start** to **Workflow result**.

<figure><img src="../.gitbook/assets/workflow-builder-workspace.png" alt="Visual workflow with Workflow start, an Iterator, a Jet Tables Create Task query, and Workflow result"><figcaption><p>The example places a Create Task query inside an iterator. The start node shows zero parameters and the result node shows zero outputs; this is an editor view, not evidence of a successful run.</p></figcaption></figure>

| Area                              | Purpose                                      |
| --------------------------------- | -------------------------------------------- |
| Function name and pencil icon     | Identify and rename the function             |
| **Workflow start**                | Inspect the function's input parameters      |
| Action and rule nodes             | Define the work and control flow             |
| **+** controls                    | Add steps at a position in the flow          |
| **Iterator** and **Iterator end** | Identify the repeated part of the flow       |
| **Workflow result**               | Inspect the outputs returned by the function |
| Undo and redo controls            | Revise changes in the visual editor          |

### Build and check the flow

1. Open **Workflow start** and configure the parameters the function needs.
2. Add the actions and rules for the process.
3. Bind action inputs to parameters or earlier step results.
4. For repeated work, configure the iterator's collection or array and use the current item's values inside it.
5. Configure **Workflow result** when the caller needs outputs.
6. Save the function, test it with representative input, and inspect the result.

In the pictured example, the **Jet Tables query — Create Task** node sits inside the iterator. Configure its required fields before executing it. Running a create action can create real records.

See [inputs](build-workflow-steps/pass-inputs-into-a-workflow.md), [outputs](build-workflow-steps/use-step-outputs-and-return-results.md), and [iterators](build-workflow-steps/process-multiple-records-with-iterators.md) for the individual concepts.

## Navigate the TypeScript editor

Select **Write Code** to work with source files instead of visual nodes.

<figure><img src="../.gitbook/assets/typescript-function-workspace.png" alt="TypeScript function editor with a Workflow Files sidebar, index.ts, and toolbar controls"><figcaption><p>The code editor shows index.ts for an existing function. Its project-specific code illustrates the workspace layout; it is not a reusable starter example.</p></figcaption></figure>

* **Workflow Files** lists the source files.
* The file tab and breadcrumb identify the file being edited, such as **index.ts**.
* The main editor contains the TypeScript implementation.
* The top toolbar provides **Run history**, **Test Function**, **Ask AI**, and **Save**.

Use the generated structure and APIs available in your editor. Define the expected inputs, return the result the caller needs, and handle empty or invalid values. Match resource and collection identifiers to your project rather than copying them from the screenshot.

## Save, test, and inspect runs

Both editors expose these controls:

| Control           | Use                                                     |
| ----------------- | ------------------------------------------------------- |
| **Save**          | Save the current function configuration or code         |
| **Test Function** | Start a test of the function                            |
| **Run history**   | Open the function's run history to inspect executions   |
| **Ask AI**        | Open AI assistance for building or editing the function |

Use this sequence:

1. Save your changes.
2. Select **Test Function** and provide the input requested by the test interface.
3. Inspect the response and any resulting record changes.
4. Open **Run history** to review the execution details available for that run.
5. Correct any problems, save, and test again.

Check a normal input, an empty input or lookup, and a failure case. A successful test of the function does not establish that an automation's trigger is configured correctly.

## Turn the function into an automation

After verifying the function, attach the trigger that should start it and configure the values it supplies. The **Add Function** dialog selects the authoring method; it does not configure the trigger.

For the trigger concepts and setup guides, see:

* [Run on a schedule](start-a-workflow/run-on-a-schedule.md)
* [Receive an incoming webhook](start-a-workflow/receive-an-incoming-webhook.md)
* [Choose a trigger](start-a-workflow/choose-a-trigger.md)

Test the actual trigger separately, then check the function's execution and resulting data. Account for repeated events and partial completion; see [Handle failures and prevent duplicate processing](handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).

Workflow functions are different from formula functions used in computed fields. For those, see [List of Functions](../user-guide/data/computed-fields/formulas/list-of-functions.md).
