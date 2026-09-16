---
icon: user-check
---

# Test and govern access

Review access as part of every release that changes users, authentication, pages, data queries, or workflows.

## Before publishing

1. Write the intended access for each audience.
2. [Review AI-generated changes](review-ai-changes.md) that affect data or authorization.
3. Use [Preview as an invited user](../../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) to inspect the app from that user's perspective.
4. Run [allowed and denied access tests](test-access.md).
5. Record the app version, environment, identities tested, and results.

Preview helps reveal differences in the interface. Use actual test sign-ins and data requests to check authentication and enforcement.

## Keep ownership clear

Assign an owner for membership reviews, authentication configuration, permission rules, and incident investigation. Recheck access when a person changes responsibilities or leaves, and after changing team or user properties used by rules.

Use [the audit trail](../audit-logs-privacy-and-security/review-the-audit-trail.md) to review available activity and [system logs](../audit-logs-privacy-and-security/investigate-system-logs.md) to investigate errors. Confirm event coverage and retention for your requirements rather than assuming the logs form a complete compliance record.

## Review the app version

Use [Version History](../../ai-app-builder/test-and-publish/version-history.md) to identify the app state being reviewed. Inspect changes before reverting, record the selected version in your review, and repeat permission tests after a revert. Check database records separately: app version history is not a record-level data backup.
