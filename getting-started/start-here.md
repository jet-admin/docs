---
icon: wand-magic-sparkles
---

# Build your first app with AI

Build a small support app that lists tickets, filters them by status, and lets you inspect a selected ticket.

## Before you begin

Use a project where you can build an app and a small test dataset. Prepare a **Tickets** table with **Name**, **Status**, **Priority**, and **Assigned to** fields. Add three clearly labeled test records: two Open tickets and one Closed ticket. Use [Jet Databases](../user-guide/jet-databases/) or an existing connected source.

[Download sample ticket records](../.gitbook/assets/sample-tickets.csv). Import them into a test table, then check the field types. The Assigned to values are demo text labels; map them to your own users if your schema uses user references.

## 1. Select your data

Open the AI Assistant and [select the connected resource](../ai-app-builder/ai-assistant/select-data-sources.md) containing Tickets. Check the table and field names before prompting.

## 2. Describe the first version

Copy and adapt this prompt:

> Build a support app using the Tickets table. Create a Tickets page with Name, Status, Priority, and Assigned to columns. Add a Status filter and a detail view for a selected ticket. Start with read-only access. Use the connected records rather than example records embedded in the page.

Wait for generation to finish. If the assistant needs more information, answer using your actual schema.

## 3. Inspect the result

Open [the Tickets page in Preview](../ai-app-builder/refine-an-app/select-a-page.md). Confirm all three test tickets appear. Choose Open in the filter and confirm only the two Open tickets remain. Open a ticket and compare its details with the source.

## 4. Make one change

> On the Tickets page, add a search field for Name. Keep the current columns and Status filter.

Search for one test ticket by its name. Alternatively, [select an element in Preview](../ai-app-builder/refine-an-app/edit-components-in-preview.md) to request a visual change.

## 5. Check appearance and access

Try [Desktop, Tablet, and Mobile](../ai-app-builder/preview-and-troubleshoot/control-app-preview.md). Apply [a theme preset](../ai-app-builder/themes-and-appearance/apply-a-theme-template.md) if needed. Use [an invited test user](../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) to inspect the app's access behavior.

## 6. Publish when ready

Follow [Preview and publish an AI app](../ai-app-builder/test-and-publish/preview-and-publish-an-ai-app.md). Repeat the ticket list, filter, detail, and access checks in the published app.

If the app fails to load or an interaction fails, inspect [Console and logs](../ai-app-builder/preview-and-troubleshoot/inspect-app-console-and-logs.md). To extend this example with an assignment action, continue with [Build a support dashboard](../ai-app-builder/practical-guides/build-a-support-dashboard.md).
