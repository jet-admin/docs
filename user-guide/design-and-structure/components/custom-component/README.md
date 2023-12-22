---
description: Build  HTML/CSS/JS, React, Vue, Angular components
---

# Custom component

## What is a Custom Component?



You can create your Custom HTML components and pass values to them from anywhere else in the application via parameters. Here is a short demo of how to do this:

1. Add an HTML component to your design
2. Add a Text Field to your design
3. From the Right Menu, change the parameter
4. Choose the correct parameter
5. Rename the parameter
6. Change the value of the HTML
7. Add a test value in the text field

{% @arcade/embed flowId="nsfWsHaoIGR6Z177IcJZ" url="https://app.arcade.software/share/nsfWsHaoIGR6Z177IcJZ" %}

## Create a Custom Component

A Custom Component uses [Web Component](https://www.webcomponents.org/introduction) specification to integrate any **JS-based** component to **Jet Admin** – this allows you to use any **Frameworks** and **Libraries** you like as long as you create them as custom **Web Components**. So it can be **React**, **Angular**, or **Vue. js-based** components, or any other.

{% content-ref url="create-a-custom-component.md" %}
[create-a-custom-component.md](create-a-custom-component.md)
{% endcontent-ref %}

## Set Custom Component Inputs

You can specify **Inputs** to pass data inside **the** Custom Component from **Jet Admin** if you have defined custom attributes for your Custom Component (Examples from GitHub include them already).

{% content-ref url="set-custom-component-inputs.md" %}
[set-custom-component-inputs.md](set-custom-component-inputs.md)
{% endcontent-ref %}

## Use Custom Component Outputs

You can specify **Outputs** to take from your Custom Component and use their values in other **Jet Admin** components**.** For such cases, you should set **Outputs** inside your Custom Component by sending **CustomEvent** with **Output** name and its value in the **detail** field (Examples from GitHub include it already).

{% content-ref url="use-custom-component-outputs.md" %}
[use-custom-component-outputs.md](use-custom-component-outputs.md)
{% endcontent-ref %}
