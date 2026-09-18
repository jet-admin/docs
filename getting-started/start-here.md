---
icon: wand-magic-sparkles
---

# Build your first app with AI

This walks you through building a working app in Jet Admin, end to end: describe it, connect your data, and publish it. You'll have something running in a few minutes.

## Before you begin

Use a project where you can build an app and a small test dataset. Prepare a **Tickets** table with **Name**, **Status**, **Priority**, and **Assigned to** fields. Add three clearly labeled test records: two Open tickets and one Closed ticket. Use [Jet Databases](../user-guide/jet-databases/) or an existing connected source.

[Download sample ticket records](../.gitbook/assets/sample-tickets.csv). Import them into a test table, then check the field types. The Assigned to values are demo text labels; map them to your own users if your schema uses user references.

## 1. Describe the app you want

From your dashboard, type what you want to build into the prompt box. Be specific about the data and the view you need — for example:

```
Create a customer support ticket management app with a ticket queue and a ticket details panel.
```

Jet generates a working interface from your description: tables, forms, and detail views, already wired to the data model it inferred from your prompt.

{% embed url="https://app.arcade.software/share/65Ipn649dh4jY6XVcAgO" %}

## 2. Connect your data

Open the AI Assistant and [select the connected resource](../ai-app-builder/ai-assistant/select-data-sources.md) containing Tickets. If you didn't already point Jet at a data source, connect one now — or start on Jet's built-in Postgres database if you don't have one ready. See [Connecting your data](../user-guide/jet-databases/) for the full list of supported sources.

{% embed url="https://app.arcade.software/share/GQxT0CLIq0OIM3t5uuOA" %}

Jet reads your schema and wires the generated tables, forms, and dashboards to read and write your real data — not a copy. Row- and column-level permissions are enforced automatically as part of this step.

## 3. Inspect the result and refine it

Open [the Tickets page in Preview](../ai-app-builder/refine-an-app/select-a-page.md). Confirm all three test tickets appear. Choose Open in the filter and confirm only the two Open tickets remain. Open a ticket and compare its details with the source.

Keep iterating with follow-up prompts (for example, on the Tickets page: "add a search field for Name, keep the current columns and Status filter"), or switch to the visual editor and click any element — like [selecting it in Preview](../ai-app-builder/refine-an-app/edit-components-in-preview.md) — to change it directly. If you need more control, drop into the code — React, Vue, or Angular — right in the editor.

{% embed url="https://app.arcade.software/share/w2kD346m0fJaytY2D6rE" %}

Along the way, try [Desktop, Tablet, and Mobile](../ai-app-builder/preview-and-troubleshoot/control-app-preview.md), apply [a theme preset](../ai-app-builder/themes-and-appearance/apply-a-theme-template.md) if needed, and use [an invited test user](../ai-app-builder/preview-and-troubleshoot/preview-as-an-invited-user.md) to check the app's access behavior.

## 4. Publish

When you're ready, publish your app. You can publish to a Jet Cloud URL or a custom domain (on paid plans) — see [Preview and publish an AI app](../ai-app-builder/test-and-publish/preview-and-publish-an-ai-app.md). Repeat the ticket list, filter, detail, and access checks in the published app.

{% embed url="https://app.arcade.software/share/oC3T6s7BGdEUinFRUSSt" %}

If the app fails to load or an interaction fails, inspect [Console and logs](../ai-app-builder/preview-and-troubleshoot/inspect-app-console-and-logs.md). To extend this example with an assignment action, continue with [Build a support dashboard](../ai-app-builder/practical-guides/build-a-support-dashboard.md).
