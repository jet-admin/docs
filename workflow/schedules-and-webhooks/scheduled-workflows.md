---
description: Run an automation at a regular interval and check its results.
---

# Scheduled Workflows

Use a schedule when work should happen without someone clicking a button—for example, checking overdue approvals each morning or syncing a table every hour. In Jet Admin, schedule and time-interval triggers are configured in the **Automation** area. The available intervals include every minute, hour, day, or month. Choose an interval that fits how often the source data changes and how quickly the result is needed.

## Set up a schedule

1. Open **Automation** in your project and add an automation.
2. Choose a schedule or time-interval trigger. Set the interval and any timing options shown in the trigger configuration. Confirm the intended time zone before relying on a daily or monthly run.
3. Add the steps the run needs: fetch records, apply a condition, and then update data or send a notification. Pass the relevant [inputs and outputs](../triggers-steps-and-parameters/inputs-outputs-parameters.md) between steps.
4. [Test individual steps and the full workflow](../test-debug-and-inspect-runs/test-and-debug.md) with representative records. Check the first scheduled run's results before leaving the automation unattended.

For example, a daily automation can query open requests, select those past their due date, and notify an owner. Store a notification timestamp or another processed marker so the next run does not send the same message again.

## Keep repeated runs predictable

A schedule may encounter the same record more than once, and a new run can begin while earlier work is still in progress. Make write and notification steps safe to repeat: filter out completed records, use a stable record key, and update a processed marker only after the action succeeds. If you shorten the interval, check the workload on connected data sources and inspect errors in [Test and Debug](../test-debug-and-inspect-runs/test-and-debug.md).

If the automation does not run when expected, check whether it is enabled, the configured timing, and the latest run result. If it runs but does nothing, inspect the filters and values passed to the first step. For other ways to start an automation, see [Schedules and webhooks](./).
