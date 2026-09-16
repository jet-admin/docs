---
icon: arrow-right
---

# Move to AI App Builder

Applies to **Classic App Builder**. Screens and recordings in this section show the Classic interface.

Assess an existing Classic app before deciding how to recreate or replace its behavior in the AI builder.

## Inventory the current app

Record its pages, components, data sources, queries, bindings, actions, workflows, custom code, authentication, and permissions. Identify the daily tasks that users depend on.

## Plan a small first scenario

1. Choose one bounded task, such as finding and updating a ticket.
2. Describe its intended audience, inputs, data rules, and expected outcome.
3. Build the corresponding AI app scenario against appropriate test resources.
4. Compare the behavior with the Classic app.
5. Verify role restrictions and record isolation.
6. Expand only after the first scenario meets the requirements.

## Compare behavior, not just layout

| Area       | What to compare                                                 |
| ---------- | --------------------------------------------------------------- |
| Data       | Filters, joins, identifiers, aggregates, and source results.    |
| Actions    | Inputs, side effects, error handling, and repeated submissions. |
| Access     | Authentication, role restrictions, and customer boundaries.     |
| Experience | Navigation, forms, empty states, and supported screen sizes.    |
| Operations | Publishing, integrations, monitoring, and recovery.             |

Do not assume automatic conversion or one-to-one component compatibility. Keep a working reference until the replacement is verified through your release process.

Use the canonical [Move from Classic to AI guide](../ai-app-builder/move-from-classic-to-ai.md) for the transition path and [AI App Builder](https://app.gitbook.com/s/-LQ08RFAKZvFADEiXKFy/ai-app-builder) for implementation.
