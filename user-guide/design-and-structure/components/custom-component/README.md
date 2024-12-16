---
description: Build HTML/CSS/JS, React, Vue, Angular components
---

# JavaScript component

## What is a JavaScript Component?

You can create your Custom JS components and pass values to them from anywhere else in the application via parameters. Here is a short demo of how to do this:

1. Add an HTML component to your design
2. Add a Text Field to your design
3. From the Right Menu, change the parameter
4. Choose the correct parameter
5. Rename the parameter
6. Change the value of the HTML
7. Add a test value in the text field

## Create a JavaScript Component

A Custom Component uses [Web Component](https://www.webcomponents.org/introduction) specification to integrate any **JS-based** component to **Jet Admin** – this allows you to use any **Frameworks** and **Libraries** you like as long as you create them as custom **Web Components**. So it can be **React**, **Angular**, or **Vue. js-based** components, or any other.

{% content-ref url="create-a-javascript-component.md" %}
[create-a-javascript-component.md](create-a-javascript-component.md)
{% endcontent-ref %}

## Set JavaScript Component Inputs

You can specify **Inputs** to pass data inside **the** Custom Component from **Jet Admin** if you have defined custom attributes for your Custom Component (Examples from GitHub include them already).

{% content-ref url="set-javascript-component-inputs.md" %}
[set-javascript-component-inputs.md](set-javascript-component-inputs.md)
{% endcontent-ref %}

## Use JavaScript Component Outputs

You can specify **Outputs** to take from your Custom Component and use their values in other **Jet Admin** component&#x73;**.** For such cases, you should set **Outputs** inside your Custom Component by sending **CustomEvent** with **Output** name and its value in the **detail** field (Examples from GitHub include it already).

{% content-ref url="use-javascript-component-outputs.md" %}
[use-javascript-component-outputs.md](use-javascript-component-outputs.md)
{% endcontent-ref %}
