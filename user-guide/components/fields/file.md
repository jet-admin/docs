---
description: In this section you will learn about Single and Multiple Files
---

# File

### Overview

To find the File component, type in "file" or scroll down

<figure><img src="../../../.gitbook/assets/image (6) (1) (2).png" alt=""><figcaption></figcaption></figure>

The file component is interactive as all inputs are, meaning you can click on the field upload a file and then download the existing file

<figure><img src="../../../.gitbook/assets/image (8) (1) (2).png" alt=""><figcaption></figcaption></figure>

### Settings

There are many things you can set up in the file component settings (click on the input to access the settings menu on the right)

#### Connecting storage

Here you can **connect** one of our native integration storages, use Jet Admin's built-in storage, or connect your own using REST API.

<figure><img src="../../../.gitbook/assets/image (5) (2) (1).png" alt=""><figcaption></figcaption></figure>

**Multipart Encoding**

Jet allows for multipart file encoding so that you can upload files with more complex data structures. You can enable multipart encoding when configuring the HTTP request for your REST API. See more about REST API [here.](https://docs.jetadmin.io/user-guide/integrations/rest-api)

#### Linking data

You can also reference dynamic values using the _`f`_ formula modal or set up a static value (upload file)&#x20;

<figure><img src="../../../.gitbook/assets/image (7) (2).png" alt=""><figcaption></figcaption></figure>

### Multiple Files

<figure><img src="../../../.gitbook/assets/image (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

Let's build an example with multiple file pickers. Follow the steps,

1. Drag and Drop **File Picker** component
2. Choose **Multiple Files**

{% @arcade/embed flowId="rKXFGFKQ4SwEdvUFxHJH" url="https://app.arcade.software/share/rKXFGFKQ4SwEdvUFxHJH" %}

### How to use File

There are many use cases for the File component, so here we'll review the most common ones:

#### Uploading to Jet Tables

We'll need a button to execute the action to upload files to Jet Tables (or any other storage). In addition, we might need a table to select the record we'll upload the file onto. This table must have a column with the `File` field type.

<figure><img src="../../../.gitbook/assets/image (4) (2).png" alt=""><figcaption></figcaption></figure>

Next, we need to tell the button where the file value will come from. For this, we'll reference the "value" attribute from the `File` filed we dropped on the canvas

{% hint style="success" %}
In this regard, `file` is just another type of Input field so you can perform all the referencing and binding actions as you would with text or other fields
{% endhint %}

To do so, follow the steps:

1. Click on the **File**
2. Click on the `Formula` icon
3. Choose **File**
4. Choose **Value**

<figure><img src="../../../.gitbook/assets/SRzgxdr.gif" alt=""><figcaption></figcaption></figure>

Now, the button will upload the file and link it to the record we selected in the table.

<figure><img src="../../../.gitbook/assets/xcfjgvuh.gif" alt=""><figcaption></figcaption></figure>

#### Displaying files

Now, if we want to **display the file** that is stored in our table, we'll need to follow the same process: go into the `File` component's settings and reference the file field from the selected row in the Table

<figure><img src="../../../.gitbook/assets/image (9) (1) (2).png" alt=""><figcaption></figcaption></figure>
