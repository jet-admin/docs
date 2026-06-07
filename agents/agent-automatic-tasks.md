---
description: >-
  Automatic Tasks allow agents to run automatically based on schedules, events,
  or predefined triggers.
---

# Agent Automatic Tasks

This is useful for recurring reports, monitoring activities, notifications, data processing, and other automated workflows without requiring manual interaction.

### Create an Automatic Task

To create a task:

1. Open **Agent Settings**
2. Navigate to **Automatic Tasks**
3. Click **Add Task**

{% @arcade/embed flowId="ZTSrOu0jCGyIASSQW86M" url="https://app.arcade.software/share/ZTSrOu0jCGyIASSQW86M" %}

### Available Triggers

Automatic tasks can be triggered in several ways:

| Trigger             | Description                            |
| ------------------- | -------------------------------------- |
| At Regular Interval | Run repeatedly at a fixed interval     |
| Based on Schedule   | Run on a specific schedule             |
| One-Time Run        | Run once at a specified time           |
| When Record Created | Run when a new record is created       |
| When Record Updated | Run when an existing record is updated |
| When Record Deleted | Run when a record is deleted           |

### Configure the Task

After selecting a trigger, configure the task settings.

Common options include:

| Setting          | Description                                       |
| ---------------- | ------------------------------------------------- |
| Schedule         | Defines when the task should run                  |
| Message to Agent | Instructions the agent should execute on each run |
| Reply Options    | Defines where task results should be sent         |

{% hint style="info" %}
### Reply Options

Task results can be:

* Do Not Reply
* Send to Slack
* Send to Telegram
{% endhint %}

### Example: Send Monthly Order Summary to Slack

The following example sends an order report to Slack once per month.

#### Configuration

| Setting          | Value                                                                             |
| ---------------- | --------------------------------------------------------------------------------- |
| Trigger          | Based on Schedule                                                                 |
| Schedule         | Once a Month                                                                      |
| Message to Agent | Generate a summary of all orders from the previous month and provide key insights |
| Reply Option     | Send to Slack                                                                     |

<figure><img src="../.gitbook/assets/image (1010).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
## How It Works

1. The task runs automatically once per month
2. The agent generates the order summary
3. The result is sent directly to the configured Slack channel
{% endhint %}

> 💡 **Common Use Cases**
>
> * Scheduled reports
> * Order summaries
> * Customer activity monitoring
> * Data quality checks
> * Daily or weekly notifications
> * Automated operational workflows
