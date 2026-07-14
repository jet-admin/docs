---
description: >-
  Learn how to connect Confluence to JetAdmin to access knowledge base content,
  manage pages, and use documentation in AI Agents and workflows.
hidden: true
---

# Confluence

Confluence is a collaboration and knowledge management platform used to create, organize, and share documentation across teams. By connecting Confluence to JetAdmin, you can search knowledge bases, manage pages and blog posts, work with attachments, and use your organization's documentation inside AI Agents and workflows.

## Connecting Confluence

To connect your Confluence account:

1. Open the **Data** tab from the left sidebar.
2. Click **Add Resource**.
3. Select **Confluence** from the list of available resources.
4. Authenticate your Confluence account.

arcade

{% hint style="info" %}
Once connected, the Confluence resource becomes available anywhere JetAdmin supports external resources.
{% endhint %}

## What can it do?

The Confluence integration gives JetAdmin access to your Confluence workspace and content.

From JetAdmin, you can:

* Search and retrieve pages
* Create and update pages and blog posts
* Access spaces and databases
* Manage tasks
* Upload and manage attachments
* Use Confluence content inside AI Agents and workflows

## Where to use it?

Confluence is most useful whenever your application needs **internal documentation**, **team knowledge**, or **collaboration content**.

You can use it in:

| JetAdmin feature   | Common use cases                                                                                |
| ------------------ | ----------------------------------------------------------------------------------------------- |
| **AI Agents**      | Answer questions using company documentation, summarize pages, search internal knowledge        |
| **Workflows**      | Create documentation automatically, update project pages, manage knowledge base content         |
| **Internal tools** | Build documentation portals, knowledge assistants, project dashboards, or internal search tools |

Typical business use cases include:

* Internal knowledge management
* Employee onboarding
* Technical documentation
* Project documentation
* Team collaboration
* SOP and policy management
* AI-powered knowledge assistants

## Available tools (Actions)

| Action                | Description                                             |
| --------------------- | ------------------------------------------------------- |
| **List Pages**        | Search Confluence pages using filters.                  |
| **Get Page**          | Retrieve a specific page by its ID.                     |
| **Create Page**       | Create a new page in a Confluence space.                |
| **Update Page**       | Update the content of an existing page.                 |
| **List Tasks**        | Retrieve tasks with filtering options.                  |
| **Get Task**          | Retrieve a specific task.                               |
| **Update Task**       | Update the status of a task.                            |
| **List Blog Posts**   | Search blog posts across your workspace.                |
| **Get Blog Post**     | Retrieve a specific blog post.                          |
| **Create Blog Post**  | Create a new blog post.                                 |
| **Update Blog Post**  | Update an existing blog post.                           |
| **Get Spaces**        | List available Confluence spaces.                       |
| **Get Database**      | Retrieve a specific database.                           |
| **Upload Attachment** | Upload a file as an attachment to a Confluence page.    |
| **List Attachments**  | List page attachments using filters.                    |
| **Get Attachment**    | Retrieve attachment metadata or download an attachment. |
| **Delete Attachment** | Delete an attachment from a page.                       |

## Example prompts for AI Agents

#### Search company documentation

```
Search Confluence for documentation about API authentication and summarize the implementation steps.
```

#### Create documentation

```
Create a new page in the Engineering space titled "Deployment Checklist" using the following content.
```

#### Update an existing page

```
Update the "Employee Onboarding" page by adding a section about VPN setup.
```

#### Summarize a project page

```
Retrieve the page with ID 123456 and provide a concise summary of the project status.
```

#### Upload documentation

```
Upload the attached PDF to the "Security Policies" page as an attachment.
```

#### Find open tasks

```
List all open Confluence tasks assigned to the Product team.
```

## Example

This example demonstrates how an AI Agent can search Confluence documentation and answer employee questions using your internal knowledge base.

arcade
