---
description: Run an automation at a regular interval and check its results.
---

# Run on a schedule

Use a scheduled automation for recurring work that does not require an app user to click a button.

## Before you start

Define the interval, the data to query, and how you will recognize completed work. Background steps need explicit inputs and queries; they cannot depend on a selected app row.

## Configure the schedule

1. Open **Automation** and add an automation.
2. Select a schedule or time-interval trigger.
3. Configure an available interval, such as every minute, hour, day, or month.
4. Check the timing options shown by the trigger. Confirm the effective time zone before relying on a particular local time.
5. Add a read action and configure its filters.
6. Pass its results into conditions or an iterator, then configure the required update or notification.

See [iterators](../build-workflow-steps/process-multiple-records-with-iterators.md) and [inputs](../build-workflow-steps/pass-inputs-into-a-workflow.md).

## Test and verify

Test the individual steps with fictional records, then verify a scheduled execution and its resulting data. Testing an action in the editor does not by itself confirm that the schedule is active.

Check the schedule's enabled state and configured interval. If the interface does not make the effective time zone clear, confirm it through a controlled scheduled test before relying on it.

## Keep repeated runs predictable

Exclude records already processed. Store a marker after successful work, and consider what happens if the next run encounters the same record. A marker alone does not guarantee duplicate prevention when runs overlap; see [repeat-safe processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).

For an end-to-end example, follow [Send scheduled reminders](../practical-guides/send-scheduled-reminders.md). For other entry points, see [Start a workflow](./).
