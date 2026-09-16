# Send scheduled reminders

Query eligible tickets on a schedule, send a reminder, and record that the reminder was sent.

## Prepare the data

This recipe assumes your test Tickets source has fields equivalent to:

| Field                              | Purpose                                   |
| ---------------------------------- | ----------------------------------------- |
| `id`                               | Stable record identifier                  |
| `status`                           | Distinguish open work from completed work |
| `due_at`                           | Decide whether the ticket is overdue      |
| `reminder_sent_at`                 | Exclude tickets already reminded          |
| Owner address or recipient mapping | Route the reminder                        |

These are example fields to create or map in your source, not fields automatically supplied by Jet Admin.

## Build the automation

1. Configure a [schedule](../start-a-workflow/run-on-a-schedule.md).
2. Query tickets whose due date is before the intended current time, whose status is open, and whose reminder marker is empty.
3. Add an iterator over the eligible records.
4. Configure an available email or messaging action for the current item's recipient. Set up the connector separately in [Data Sources](../../user-guide/data-sources/).
5. After the message action succeeds, update that ticket's reminder marker.
6. Test using a destination you control.

Use the date comparison and current-time functions supported by your source or formula editor. Confirm the relevant time zone.

## Verify four cases

* An overdue, open ticket without a marker receives a reminder.
* A completed ticket is excluded.
* A future-due ticket is excluded.
* A ticket already reminded is excluded.

This recipe sends one reminder per marker. If you need recurring reminders, define when the next reminder becomes eligible instead of leaving the marker permanently set.

If sending succeeds but saving the marker fails, a later run may send again. See [partial success and duplicate prevention](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).
