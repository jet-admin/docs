---
description: >-
  Learn how to connect Fellow to JetAdmin to access meeting recordings, notes,
  transcripts, and workspace information from AI Agents and workflows.
hidden: true
---

# Fellow

Fellow is an AI meeting assistant that records, transcribes, and summarizes meetings while helping teams capture decisions, action items, and meeting notes. By connecting Fellow to JetAdmin, you can access meeting content, recordings, and transcripts directly from AI Agents and workflows.

## Connecting Fellow

To connect your Fellow account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Fellow** from the list of available resources.
4. Authenticate your Fellow account.

arcade

{% hint style="info" %}
Once connected, the Fellow resource becomes available anywhere JetAdmin supports Data resources.
{% endhint %}

## What can it do?

The Fellow integration gives JetAdmin access to your meeting data and workspace information.

From JetAdmin, you can:

* Access meeting recordings and transcripts
* Retrieve meeting notes
* Search past meetings
* View workspace and user information
* Use meeting knowledge inside AI Agents and workflows

## Where to use it?

Fellow is most useful whenever your application needs **meeting context**, **AI-generated notes**, or **team knowledge**.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| **AI Agents**      | Answer questions about past meetings, summarize discussions, retrieve action items and decisions |
| **Workflows**      | Automate meeting reporting, archive notes, share summaries, or process meeting transcripts       |
| **Internal tools** | Build meeting dashboards, searchable transcript libraries, or internal knowledge assistants      |

Typical business use cases include:

* Meeting summaries
* Knowledge management
* Project tracking
* Team collaboration
* Action item follow-up
* Customer meeting insights
* Internal documentation

## Available tools (Actions)

| Action              | Description                                                                   |
| ------------------- | ----------------------------------------------------------------------------- |
| **Get Me**          | Retrieve information about the authenticated user and their Fellow workspace. |
| **List Recordings** | Search meeting recordings using filtering options.                            |
| **Get Recording**   | Retrieve a specific meeting recording, including its transcript.              |
| **List Notes**      | Search meeting notes using filters.                                           |
| **Get Note**        | Retrieve the full content of a specific meeting note.                         |

## Example prompts for AI Agents

#### Summarize a meeting

```
Retrieve the latest meeting recording from Fellow and summarize the key decisions and action items.
```

#### Search meeting notes

```
Find meeting notes related to the Q3 product roadmap and summarize the discussion.
```

#### Retrieve a transcript

```
Get the transcript from yesterday's engineering meeting and list all follow-up tasks.
```

#### Review customer meetings

```
List all customer meeting recordings from the past month and summarize the most common feature requests.
```

#### Read meeting notes

```
Retrieve the meeting note titled "Weekly Leadership Sync" and provide a concise executive summary.
```

#### Get workspace information

```
Retrieve my Fellow workspace information and identify the current authenticated user.
```

## Example

This example demonstrates how an AI Agent can retrieve a meeting transcript from Fellow and generate a concise summary with decisions and action items.

arcade
