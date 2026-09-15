---
description: Start an automation when an external service sends an HTTP event.
---

# Webhooks

An incoming webhook starts a Jet Admin automation when another system sends an HTTP request to its trigger URL. Use it when the work should begin as an event happens—for example, after a new order arrives or a support ticket changes status. For work that should run at a regular interval, use a [scheduled workflow](scheduled-workflows.md).

## Connect an event

1. Open **Automation** in your project, add an automation, and choose a webhook trigger.
2. Copy the URL and follow the request method and payload format shown in the trigger configuration. Add that URL to the sending service's webhook settings for the event you want to handle.
3. Inspect a sample event. Identify the fields later steps actually need, such as an `order_id` or `status`, and pass them into the workflow. Fetch the current record when you need details beyond the event payload.
4. Add a condition before any write action so unrelated or incomplete events do not change data. Then [test the steps and the full workflow](../test-debug-and-inspect-runs/test-and-debug.md) with a representative request from the sender.
5. Check the resulting run and its inputs. Also send a second copy of the event to confirm that a duplicate cannot repeat a notification or update unexpectedly.

Treat the trigger URL as a credential: share it only with the sender and rotate or replace it if exposed. If the sender supports request authentication, configure it according to the options offered by your Jet Admin webhook trigger. Do not put secrets in the payload or in a page visible to app users.

## Example and troubleshooting

A ticket service can send a `ticket.updated` event with a ticket ID. The automation fetches that ticket, checks whether it moved into an escalation state, and alerts the assigned team once. A stored processed event ID or escalation timestamp prevents a retried request from sending the same alert twice.

If no run appears, confirm that the sender called the correct URL with the expected method and that the event subscription is active. If a run starts but a step fails, inspect the incoming payload, missing fields, data-source permissions, and the highlighted error in [Test and Debug](../test-debug-and-inspect-runs/test-and-debug.md). For the rest of the workflow, see [Triggers, steps, and parameters](../triggers-steps-and-parameters/).
