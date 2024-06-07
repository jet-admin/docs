---
description: A detailed overview of the types of Actions.
---

# Actions

Action is an operation that you can perform in Jet Admin. Visually, the action is a button in the Jet Admin interface.

To add an action you need to&#x20;

1. Select a Button component&#x20;
2. Drag and drop it on the page

{% @arcade/embed flowId="i0thUp5Um7Dt4k0G8ga1" url="https://app.arcade.software/share/i0thUp5Um7Dt4k0G8ga1" %}

## Action types

There are 14 types of actions:&#x20;

* **Run operation**. Perform any CRUD operation or custom API/SQL query.&#x20;
* [**Run Workflow**](../workflow/). Fires a sequence of events.
* **Navigate to page**. Passing values and switching between pages.
* **Open URL.** Open the link in a new or the current tab.
* [**Open Modal/Close Modal**](../components/modal.md)**.** Open or close the pop-up modal window.
* [**Run Component Action**](../components/component-actions.md)**.** Act on a component, such as updating data or clearing the form after submitting.
* [**Show Notification**](../components/custom-notifications.md)**.** Show custom notification.
* [**Set Variable**](../binding-and-values/temporary-and-stored-variables.md#set-a-variable). Set a value to a specific Page Variable or Page Variable .&#x20;
* [**Run JavaScript**](actions.md#run-javascript). Execute a JavaScript code.&#x20;
* **Copy to Clipboard**. Copy data to your Clipboard.&#x20;
* **Export Data.** Export data from the table.
* **Import Data**. Import data to a collection.&#x20;
* **Download File.** Download the file from the API call.

<div align="left">

<figure><img src="../../.gitbook/assets/image (923).png" alt=""><figcaption></figcaption></figure>

</div>

## Action confirmation dialog

You can set up a confirmation dialog that will appear before executing an action.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Confirmation dialog example</p></figcaption></figure>

To add a confirmation dialog, use the "Confirm on execute" section of the right-side panel

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can define the Title, Description, and button styles for your confirmation dialog.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Run Operation

Perform operation with your resources, such as CRUD operations with Databases, operations with third party services, APIs and frameworks, and operations with storages.

#### Creating an operation in a button

1. Click on the **Button**
2. Go to the **Click Action**
3. Choose **Run Operation**
4. Choose the **Resource**
5. Choose the **Action**

{% @arcade/embed flowId="hiEUE1MH878JTe5ffe6h" url="https://app.arcade.software/share/hiEUE1MH878JTe5ffe6h" %}

#### Operations with storages

<figure><img src="../../.gitbook/assets/image (942).png" alt=""><figcaption><p>Storages operations</p></figcaption></figure>

You can perform these actions with storages:

* Getting private file URL
* Uploading a File
* Getting list of objects
* Creating a directory
* Removing an object

### Navigate to Page

You can pass values and switch between pages. To do so, follow the steps:

1. Click on the Button
2. Go to the **Click Action**
3. Choose **Navigate to Page**
4. Choose the **Link of the Page**

{% @arcade/embed flowId="yxx0Jn0fHFHMr0z3wb7O" url="https://app.arcade.software/share/yxx0Jn0fHFHMr0z3wb7O" %}

### Open URL

Opens any website URLs, use **Action** specified as **Open URL**.

1. Click on the Button
2. Go to the **Click Action**
3. Choose **Open URL**
4. Click on the URL icon to change the **URL of the Page**

{% @arcade/embed flowId="XEOidwMdpzMphdDs7lpw" url="https://app.arcade.software/share/XEOidwMdpzMphdDs7lpw" %}

### Open/Close Modal

{% @arcade/embed flowId="7bf7uWU3nOnGSNBOeSkG" url="https://app.arcade.software/share/7bf7uWU3nOnGSNBOeSkG" %}

You can close the pop-up modal window. To do so, follow the steps:

1. Click on the **Button**
2. Go to the **Click Action**
3. Choose **Close Modal**

{% @arcade/embed flowId="YpWbACsL2fhufqFzWLyY" url="https://app.arcade.software/share/YpWbACsL2fhufqFzWLyY" %}

{% content-ref url="../components/modal.md" %}
[modal.md](../components/modal.md)
{% endcontent-ref %}

### Run Component Action

You can act on a component, such as updating data or clearing the form after submitting.

{% content-ref url="../components/component-actions.md" %}
[component-actions.md](../components/component-actions.md)
{% endcontent-ref %}

### Show Notification

You can show custom notifications.

{% content-ref url="../components/custom-notifications.md" %}
[custom-notifications.md](../components/custom-notifications.md)
{% endcontent-ref %}

### Run JavaScript

To execute JavaScript code upon clicking a button, follow these steps:

1. Click on the button.
2. Navigate to the Click Action.
3. Select "Run JavaScript."
4. Type your JavaScript code and return the result.

<div align="left">

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\
You can Insert input values from other components and use it further within your JavaScript code. To do that, click 'Insert Input' and choose the needed component.

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Export Data

You can export data from the table. To do so, follow the steps:

1. Click on the **Table**
2. Go to the `Actions Tab`
3. Scroll down to the **Header Actions**
4. Click on the `New Action`
5. Choose **Export Data**
6. Choose the **Resource** and the **Collection**

{% @arcade/embed flowId="1Q2l8eurRAfAenociloS" url="https://app.arcade.software/share/1Q2l8eurRAfAenociloS" %}

### Download File

1. Click on the **Button**
2. Go to the **Click Action**
3. Choose **Download File**

{% @arcade/embed flowId="XO6aKLkHar5GxSw8zbMT" url="https://app.arcade.software/share/XO6aKLkHar5GxSw8zbMT" %}

Now, let's define the Resource and Operation. To do so, follow the steps:

1. Click on the button
2. Pick a resource&#x20;
3. Choose an operation to write SQL queries
4. Write the SQL query
5. Click on the Run button
6. Click on the Save button

This will generate a JSON file with the data.

{% @arcade/embed flowId="xx2LzwkiSKjxpFTs5v7f" url="https://app.arcade.software/share/xx2LzwkiSKjxpFTs5v7f" %}

### Copy to clipboard

You can set up actions to copy data to the clipboard. This works with all components. To configure it, follow the steps:

1. Go to the **Actions Tab**
2. Go to the **Row Click**
3. Choose **Copy to Clipboard**&#x20;
4. Click on the `Set up with Formula` icon
5. Choose **Email**

{% @arcade/embed flowId="9Ht0CPoM0ZmenIUSZx03" url="https://app.arcade.software/share/9Ht0CPoM0ZmenIUSZx03" %}

