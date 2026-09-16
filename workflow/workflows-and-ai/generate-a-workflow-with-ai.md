---
description: Creating workflows using the Ask AI feature
---

# Generate a workflow with AI

Use **Ask AI** to draft workflow steps from a plain-language description, then review and test the result.

## Open Ask AI

1. Configure a supported trigger and open its workflow builder.
2. Select **Ask AI**.
3. Describe the available resource, input, condition, and desired result.

{% @arcade/embed url="https://app.arcade.software/share/Sd6L8bPYmjApw4sEQ7on" flowId="Sd6L8bPYmjApw4sEQ7on" %}

## Write a specific request

For a Tickets example:

> Use the ticket\_id input to find one record in my Tickets collection. If the record exists and its status is Open, change its status to In progress. If no record matches, do not update anything. Use the actual resource and field names available in this project.

Replace the example names and status values with your own. Describe the expected behavior for empty results, not just the successful path.

## Review the generated steps

Check the resource and collection, record ID binding, condition values, and write fields. Ensure the generated process targets only the intended record.

The existing walkthrough below shows a customer-email use case. It illustrates generation and review; it is a different example from the Tickets prompt.

{% @arcade/embed url="https://app.arcade.software/share/kIdVDgdbOWiisMcS83oy" flowId="kIdVDgdbOWiisMcS83oy" %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-08-31 165254.png" alt=""><figcaption></figcaption></figure>

## Test the result

Use a matching ticket, a ticket with another status, and a missing ID. Verify the stored data after each test. Review recipients before testing generated notification actions.

Generating a workflow does not add an agent that makes decisions at runtime. For that pattern, see [Run an agent in a workflow](../../ai-agents/run-agents-in-apps-workflows-and-tasks/workflows-with-agents.md).
