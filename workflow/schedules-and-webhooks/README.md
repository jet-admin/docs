# Schedules and webhooks

A [scheduled workflow](scheduled-workflows.md) runs on a configured schedule. A [webhook](webhooks.md) starts a workflow after an external event. Choose the one that matches how the process should begin.

For scheduled work, verify time zone, frequency, and whether another run could overlap. For webhooks, check the sender, authentication, payload, and what happens if the same event arrives twice. Inspect the parameters passed into later steps. Test with representative payloads and records, then use Test, debug, and inspect runs to check outcomes.
