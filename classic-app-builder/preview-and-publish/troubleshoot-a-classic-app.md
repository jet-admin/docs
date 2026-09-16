---
icon: wrench
---

# Troubleshoot a Classic app

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Trace a problem from the visible component to the value, action, or data request responsible for it.

| Symptom                             | Check first                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------ |
| Component is empty                  | Resource result, active filters, field mapping, and empty-state configuration. |
| Form shows the wrong record         | Selected row, bound field, and record identifier.                              |
| Filter has no effect                | Referenced output, value type, comparison, and other filters.                  |
| Button appears to do nothing        | Click Action, required inputs, confirmation, and operation result.             |
| Data changes but the UI looks stale | Post-action refresh and the component's data source.                           |
| A user sees different content       | Identity, team, dynamic filters, visibility, and enforced permissions.         |
| Published app differs from Preview  | Target environment, published address, and release state.                      |

## Reproduce and isolate

1. Record the page, component, user role, environment, and failure time.
2. Use one synthetic record and a repeatable action.
3. Inspect the source value before checking the target binding.
4. Inspect action inputs before changing the action.
5. Check the resource result and available logs.
6. Make one targeted correction and repeat the same test.

For UI bindings, use [Data binding and variables](../binding-and-values/). For behavior, use [Actions and logic](../actions-and-logic/). For release problems, use [Publish & Deploy troubleshooting](../../jet-bridge-deployment/logs-and-troubleshooting/).

A hidden control and a denied request are different outcomes. Repeat allowed and denied [access tests](../../access-and-sharing/overview/test-access.md) after changes.
