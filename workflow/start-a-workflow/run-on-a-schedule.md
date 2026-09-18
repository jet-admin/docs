---
description: Run an automation at a regular interval and check its results.
---

# Run on a schedule

Use **Workflows → Add Automation** to choose when background work starts. Background logic needs explicit inputs and queries; it cannot depend on a row selected in an app.

## Choose a timing option

| Option                   | Configuration                                                                    | Use                                |
| ------------------------ | -------------------------------------------------------------------------------- | ---------------------------------- |
| **At regular intervals** | **Interval in minutes**                                                          | Repeat a check at a fixed interval |
| **Based on a schedule**  | **Every day**, **Days of the week**, **Days of the month**, or **Specify dates** | Run according to a calendar        |
| **One-time run**         | **Run date**                                                                     | Arrange one execution              |

The inspected interval form initially shows 15 minutes. Set the value needed for your process instead of relying on that initial value.

## Configure a daily schedule

1. Open **Workflows** and select **Add Automation**.
2. Choose **Based on a schedule**.
3. Choose **Every day** and set **Time**.
4. The inspected daily form specifies **Time zone is UTC (+0)**. Convert your intended local time to UTC; consider daylight-saving changes when relevant.
5. Configure the function's logic and required data.
6. Save the function and complete the trigger configuration shown in your app.

The UTC label above was verified for the daily form. Check the labels for other schedule modes and the one-time date picker before assuming they use the same time zone.

For recurring work, start with a query that selects only the records due for processing. Pass those results into [conditions](../build-workflow-steps/add-conditions-and-branches.md) or an [iterator](../build-workflow-steps/process-multiple-records-with-iterators.md).

## Test the function and the schedule separately

Use fictional records in a test environment. Save and test the function with representative inputs, then check an actual scheduled execution in **Run history** and verify its result. An editor test does not prove that a schedule is active.

Record the configured time, expected execution time, observed run, and result. Check the trigger's saved configuration and any enabled-state control available in your interface if the run does not appear.

## Keep repeated runs predictable

Exclude records already processed and store a marker after successful work. A marker alone does not prevent duplicate work when executions overlap. See [Handle failures and prevent duplicate processing](../handle-outcomes/handle-failures-and-prevent-duplicate-processing.md).

For an application example, see [Send scheduled reminders](../practical-guides/send-scheduled-reminders.md). For other entry points, see [Choose a trigger](choose-a-trigger.md).
