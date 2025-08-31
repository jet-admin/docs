---
description: >-
  Explore how Jet Admin's RestAPI Builder seamlessly processes various response
  outputs from endpoints.
---

# Endpoint Response Outputs

In Jet Admin's RestAPI Builder, endpoints can return data in four different formats: JSON, XML, Text, and Blob. Each format serves specific purposes and is compatible with Jet Admin's capabilities for accepting data from endpoints.

<figure><img src="../../../.gitbook/assets/image (977).png" alt=""><figcaption></figcaption></figure>

### **JSON (JavaScript Object Notation)**

**When to Use:** Jet Admin accepts JSON-formatted data from endpoints when it needs to retrieve structured data, such as objects or arrays.

### **XML (eXtensible Markup Language)**

**When to Use:** If endpoints return data in XML format, Jet Admin can handle it effectively. XML format is used when the data requires a hierarchical structure and needs to be compatible with systems using this format.

### **Text**

**When to Use:** Jet Admin accepts text data from endpoints for various purposes, including returning simple messages, logs, or raw content.

### **Blob (Binary Large Object)**

**When to Use:** When endpoints return binary data that needs to be downloaded or processed by the client, Jet Admin accepts Blob format. This allows for seamless handling and management of Blob data within the platform.

{% hint style="info" %}
**Choosing the Right Response Output:**

Select the appropriate response output format (JSON, XML, Text, or Blob) based on the structure and type of data returned by your endpoints.
{% endhint %}

By accepting data in these four response output formats, Jet Admin enables efficient processing, visualization, and use of data received from endpoints within the platform.
