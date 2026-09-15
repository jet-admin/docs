# Govern AI-generated apps

An AI-generated app needs the same access and review as any production app. A prompt can create pages, queries, actions, workflows, or agent tools; inspect those outputs before users rely on them.

1. Identify the app’s data sources and the credentials used to read or change records.
2. Review generated queries, API calls, and write actions. Confirm their parameters and intended effects with safe test data.
3. Define who may sign in, which pages and records each role may see, and which actions each role may run.
4. Test as representative roles, including an end user if the app is a portal. Try a restricted record and a restricted action.
5. Use [Audit logs](audit-logs-privacy-and-security/audit-logs.md) and relevant run history to inspect behavior after release.

Follow [Authentication and SSO](authentication-and-sso/), [App and data permissions](app-and-data-permissions/), and [Data Privacy & Security](audit-logs-privacy-and-security/data-privacy-and-security.md). If an app uses agents, [test them safely](../ai-agents/test-an-agent-safely.md) with their actual tools and access.
