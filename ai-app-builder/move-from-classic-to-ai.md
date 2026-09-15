# Move from Classic to AI

An existing Classic app may already contain useful data connections, roles, and business rules. Treat those as requirements for a new AI build rather than assuming the generated app will reproduce them automatically.

1. Inventory the current app: data sources, pages, binding, variables, actions, workflows, permissions, and publishing setup.
2. Choose one task to rebuild in a separate AI app. Connect a test source and write a prompt using the current schema and user roles.
3. Compare the result with the Classic behavior. Test every read, write, and restricted view involved in that task.
4. Ask for focused changes, then verify again. Move the next task only when the first is ready for use.
5. Plan how users will switch to the new app and keep the Classic app available until the change is complete.

See Maintain an existing Classic app for the legacy editor. For a first AI build, use [Build your first app with AI](../getting-started/start-here.md).
