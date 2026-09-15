---
icon: flask
---

# Test an agent safely

Before an agent uses live data or external tools, run a controlled task with safe records and limited credentials.

1. Give the agent a concrete objective and expected result. Test a normal request first.
2. Inspect which tools it uses, the parameters it sends, and the data it reads. Keep write tools disabled or scoped to test records until reviewed.
3. Try missing context, an irrelevant request, and a request for a record it should not access. Check how the agent responds when it cannot complete the task.
4. Test any workflow trigger or channel that will invoke the agent. Verify the same permissions apply there.
5. Record the prompt, outcome, and tool calls. Revise instructions or access, then repeat the case.

Use [Audit logs](../access-and-sharing/audit-logs-privacy-and-security/audit-logs.md) and relevant run history when available. For app access, see [Govern AI-generated apps](../access-and-sharing/overview.md).
