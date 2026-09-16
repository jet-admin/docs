---
description: Start an automation when an external service sends an HTTP event.
---

# Receive an incoming webhook

An incoming webhook starts an automation when an external service sends an HTTP request to the trigger URL.

## Configure the trigger

1. Open **Automation**, add an automation, and select a webhook trigger.
2. Copy its URL into the sending service's webhook configuration.
3. Use the request method, content type, and payload format required by the trigger.
4. Send a fictional test event and inspect the values it supplies.
5. Map the required values into later steps.

Treat the trigger URL as a credential. Keep it out of screenshots and public examples. Configure sender authentication only using options supported by the actual trigger; do not assume a particular signature scheme.

## Map a ticket event

This illustrative JSON describes a simple event contract, not a required Jet Admin payload schema:

```json
{
  "event_id": "evt_demo_001",
  "event_type": "ticket.updated",
  "ticket_id": 1,
  "status": "Escalated"
}
```

1. Read the fields as they appear in the received payload; the sender may nest them differently.
2. Check the event type and require a ticket ID before changing data.
3. Fetch the ticket by ID when later steps need its current state.
4. Configure the action using the fetched record or validated event values.
5. Track the event ID if your process must recognize duplicates.

Match status values to your source. See [input mapping](../build-workflow-steps/pass-inputs-into-a-workflow.md) and [duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).

## Verify the complete path

Send a normal event, an event without the required ID, and a second copy of the normal event. Check the action results and stored records. Decide explicitly how malformed and duplicate events should be handled.

## Troubleshoot

* **Nothing happens:** check the sender's request result, trigger URL, method, payload format, and active configuration.
* **The wrong data is used:** inspect the received field paths and their types.
* **A repeated event repeats an action:** inspect your event tracking and the sender's delivery behavior.

For periodic work, use a [schedule](run-on-a-schedule.md).
