---
icon: arrow-right-arrow-left
---

# Move from Classic to AI

Use the existing Classic app as a set of requirements for a separate AI build. Do not assume a prompt automatically reproduces its configuration.

## Rebuild one task

1. Inventory its sources, pages, fields, actions, workflows, permissions, and publishing setup.
2. Choose one small task and prepare test data.
3. Follow [Build your first app with AI](../getting-started/start-here.md) using the same field names and business rules.
4. Compare the new app with the Classic task.
5. Test reads, writes, and restricted access before moving to the next task.

## Plan the switch

Record remaining differences and decide how users will move to the new app. Keep the existing app available until the replacement has passed the required checks.

| Requirement           | Check                                             |
| --------------------- | ------------------------------------------------- |
| Data source           | Reads and writes reach the intended system.       |
| Business rules        | Validation and workflow outcomes match.           |
| Access                | Restricted records and actions remain restricted. |
| Navigation and layout | Users can complete the task on their devices.     |

Use [Maintain an existing Classic app](../classic-app-builder/maintain-an-existing-classic-app.md) for legacy-editor work. Continue with [Test and publish](test-and-publish/) for the new AI app.
