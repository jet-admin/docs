---
description: In this section you will learn about Iterators
---

# Iterators

Iterators are a powerful tool in Jet Admin and can be implemented in both automation and Workflow. An iterator can cycle through a collection or an array of data and process steps individually for each item.

## Iterator Use Cases

Iterators can be created in [automations or workflows](./). You can add automation in the _Automation_ menu on the left, and workflows can be added to components in the _Actions_ menu of a given component.&#x20;

{% hint style="info" %}
Workflows are activated by actions and can only be edited within the _Actions_ menu of the component they are applied to.
{% endhint %}

{% hint style="info" %}
Automations is more general and good for purposes such as sending Slack notifications when data changes.
{% endhint %}

### Use Cases in Automations

* Send emails with coupons to customers who left positive/negative ratings
* Create a table that updates automatically every hour with a list of active users
* Keep a table updated with items that are in stock at your store or online shop
* Send a Slack message to your team when important data is updated

### Use Cases in Workflows

* [Send emails to customers that are presented in a filtered table](iterators.md#example-of-a-workflow-with-an-iterator)
* A button that will get data for the current day, analyze it with OpenAI, and save results to a table

## Creating an Iterator&#x20;

Add an iterator and the steps that you want to iterate over to your workflow or automation. You can also add the iterator later and drag and drop the steps into it.

### Adding an Automation with Iterator

1. Click on the **Automation icon**
2. Click on the `Add automation`&#x20;
3. Choose a trigger for your automation or workflow
4. Add an iterator as a step

{% @arcade/embed flowId="QP5qx9WJgYAGSaSnoQix" url="https://app.arcade.software/share/QP5qx9WJgYAGSaSnoQix" %}

### Iterator Settings

<figure><img src="../../.gitbook/assets/image (941).png" alt=""><figcaption><p>Iterator settings</p></figcaption></figure>

Iterators can work in two modes: "[Load Data](iterators.md#load-data-type)" and "[Specify Iterate](iterators.md#specify-iterate-type)".

#### Load Data Type

This type of iterator will get data to iterate from any resource that you have.&#x20;

You can choose a resource, a collection and use filters to get the precise data you want to cycle through.

{% hint style="info" %}
Refer to the [resources article](../integrations/) to learn more about how resources work.
{% endhint %}

#### Specify Iterate Type

This type of iterator will use any array of data, that you can get from previous steps or from workflow parameters.

It could be simple arrays, or arrays of objects.

{% hint style="info" %}
Refer to the [Inputs, Outputs, Parameters](inputs-outputs-parameters.md) article to learn more about them
{% endhint %}

## Example of a Workflow with an Iterator

Let's create a button as a table header that will trigger a workflow which will iterate through a collection of customers that are filtered with a multiple select field of cities and send emails to them.

<figure><img src="../../.gitbook/assets/image (940).png" alt=""><figcaption><p>A table with customers, multiple-select filter and button with a workflow action</p></figcaption></figure>

### Pre-requisites

* A table with data, containing a column with emails
* A working filter that will be filtering the table

#### Gathering pre-requisites

{% @arcade/embed flowId="S6oREqJWf6Dzv91I9xVD" url="https://app.arcade.software/share/S6oREqJWf6Dzv91I9xVD" %}

Steps:

1. Have a table with a collection of items that you would want to iterate through, such as a table with customers with data for cities and their emails.
2. Create a component that will be used to filter out the table. Such as a multi-select with cities.
3. Load the data for your multi-select component dynamically from another collection, or pre-define them.
4. Use your multi-select component value as a filter for your table

### Creating a Workflow with Iterator

{% @arcade/embed flowId="CyuvyHn4OULwyYZZKc0o" url="https://app.arcade.software/share/CyuvyHn4OULwyYZZKc0o" %}

Steps:

1. Have a table component to be used as our source of data and a filter. Such as customers table that are getting filtered by multiple cities.
2. Create a new action that will be performing a workflow with an iterator. One of the options is to have a button as a table header.
3. In the workflow builder, create a parameter to pass selected emails. It's better to use parameter with the same type as your filter on a page, which is multiple select.
4. Optionally add a test value to your workflow parameter with an array of at least two cites
5. Create an iterator that will load data from the same collection and use workflow parameter as a filter.
6. Create a notification inside the iterator to show current collection items email and test the workflow.
7. Create an action that will send the email to current collection items email.
8. Optionally create a delay.
9. Pin the button to the table as a header.

####
