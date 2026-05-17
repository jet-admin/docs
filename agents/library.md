---
description: >-
  The Library in JetAdmin allows you to upload and manage files that agents can
  use as a knowledge source.
---

# Library

These files are processed and summarized automatically, making it easier for agents to understand and use large amounts of information.

### Accessing the Library

To open the Library:

1. Go to **Data**
2. Scroll down and click **Library**

{% @arcade/embed flowId="lFVwtnOw4MychbWoyiz1" url="https://app.arcade.software/share/lFVwtnOw4MychbWoyiz1" %}

### Adding Files

Uploading files is simple:

1. Click the **+** button
2. Upload your file
3. The system will process and summarize the content automatically

<figure><img src="../.gitbook/assets/image (996).png" alt=""><figcaption></figcaption></figure>

### Importing Websites

You can also import website content into the Library.

1.  Click _Upload or Import_ button<br>

    <figure><img src="../.gitbook/assets/image (1008).png" alt=""><figcaption></figcaption></figure>
2. Select Import Website
3. Enter the website URL
4. Configure periodic sync settings (optional)
5. Click Import Website

<figure><img src="../.gitbook/assets/image (1009).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
#### Advanced Settings

Advanced settings allow you to control website crawling:

* **Pages limit:** Maximum number of pages to crawl
* **Crawl depth:** Maximum crawl depth
* **Include paths:** Crawl only selected paths
* **Exclude paths:** Ignore selected paths
{% endhint %}

> **When to Use Website Import**
>
> Website import is useful when your documentation, help center, knowledge base, or public content is already available online and should stay automatically updated for your agents.

### Using Library with Agents

Libraries can be connected to agents to provide additional context and knowledge.

To add a library to an agent:

1. Open your agent settings
2. Go to **Libraries** section
3. Click **+ Library**
4. Select the Library you want to connect

{% @arcade/embed flowId="AW5EDOuONT60jX3WitgJ" url="https://app.arcade.software/share/AW5EDOuONT60jX3WitgJ" %}

### Why Use Library

Libraries help agents:

* Understand large datasets or documents
* Answer questions based on your internal knowledge
* Provide more accurate and context-aware responses

{% hint style="info" %}
#### 💡 Best Practice

Clearly define in your agent instructions how the library should be used (e.g. when to search, what to extract, and how to respond).
{% endhint %}
