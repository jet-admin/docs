---
description: >-
  Learn how to connect Granola to JetAdmin to access meeting notes, transcripts,
  and workspace data from AI Agents and workflows.
---

# Granola

Granola is an AI-powered meeting assistant that captures conversations, generates notes, and organizes meeting knowledge. By connecting Granola to JetAdmin, you can search meetings, retrieve transcripts, and use meeting context inside AI Agents and workflows.

## Connecting Granola

To connect your Granola account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Granola** from the list of available resources.
4. Authenticate your Granola account.

{% @arcade/embed flowId="q4G10OxLZL4SSSJYEft5" url="https://app.arcade.software/share/q4G10OxLZL4SSSJYEft5" %}

{% hint style="info" %}
Once connected, the Granola resource becomes available anywhere JetAdmin supports Data resources.
{% endhint %}

## What can it do?

The Granola integration gives JetAdmin access to your meeting history and workspace information.

From JetAdmin, you can:

* Browse and search meetings
* Read meeting notes and transcripts
* Access meeting folders
* Query meetings using natural language
* View account information
* Use meeting knowledge inside AI Agents and workflows

## Where to use it?

Granola is most useful whenever your application needs meeting context, conversation history, or AI-generated meeting notes.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| **AI Agents**      | Answer questions about past meetings, summarize discussions, retrieve decisions and action items |
| **Workflows**      | Automate meeting reporting, organize meeting records, or generate follow-up summaries            |
| **Internal tools** | Build searchable meeting archives, knowledge assistants, or team collaboration dashboards        |

Typical business use cases include:

* Meeting summaries
* Knowledge management
* Project tracking
* Team collaboration
* Customer meeting reviews
* Action item tracking
* Internal documentation

## Available tools (Actions)

| Action                      | Description                                                   |
| --------------------------- | ------------------------------------------------------------- |
| **Get Account Info**        | Retrieve information about the authenticated Granola account. |
| **List Meeting Folders**    | List available folders used to organize meetings.             |
| **List Meetings**           | Retrieve meetings with filtering options.                     |
| **Query Meetings**          | Search meetings using natural language queries.               |
| **Read Meeting Transcript** | Retrieve the transcript of a specific meeting.                |
| **Read Meetings**           | Retrieve detailed information about one or more meetings.     |

## Example prompts for AI Agents

#### Summarize a recent meeting

```
Retrieve my latest Granola meeting and summarize the key decisions, action items, and next steps.
```

#### Search meeting history

```
Find meetings where we discussed API authentication and summarize the outcomes.
```

#### Read a meeting transcript

```
Read the transcript from yesterday's product meeting and list all assigned action items.
```

#### Review customer conversations

```
Search customer meetings from the past month and summarize the most frequently requested features.
```

#### Organize meetings

```
List all meeting folders and show how many meetings are stored in each one.
```

#### Query meeting knowledge

```
Search my Granola meetings for discussions about the Q4 roadmap and provide a summary with relevant meeting links.
```
