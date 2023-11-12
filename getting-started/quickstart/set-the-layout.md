---
description: Discover how to utilize components to build your app's user interface
---

# Build UI

Components are prebuilt UI elements your users engage in, such as `Tables`, `Forms`, `Buttons`. In this example, only a limited number of components are used; you can explore 50+ Components in the UI Component Library. Drag-and-drop components within **Layout** `Columns`, `Tabs`, and `Modals`, facilitating the building of your app.

You'll be building an app that enables the creation and updating of **Deals** data. To enable this functionality, you'll add `Table`, `Forms`, and `Modals`. Learn more about [Jet UI Concept](../../user-guide/jet-ui/) in our documentation. Additionally, if you want to implement this functionality swiftly (Create, Update, Delete flow), you can generate it in seconds using [Page Templates](../ui-in-seconds.md).

### Set the Layout

`Columns` are used to set the horizontal component of the layout. You can add multiple columns and resize them.&#x20;

{% @arcade/embed flowId="qqlSdR0LVUOSNZRMPOO4" url="https://app.arcade.software/share/qqlSdR0LVUOSNZRMPOO4" %}

### Display Deals

When you select the **Table** component, the right panel automatically updates to display the properties of the component. Components come with a wide range of properties that you can configure. Properties are accessible from other components and queries, allowing for a more integrated and dynamic user interface experience.&#x20;

Click **Data Source** – **Jet Tables** and the **Deals** collection that you've created.

{% @arcade/embed flowId="jU26kc5IVQRR4HeOLBMj" url="https://app.arcade.software/share/jU26kc5IVQRR4HeOLBMj" %}

Modify the **Logo** column to have a circular frame and position it as the first column.

{% @arcade/embed flowId="2SmD0N6RcbanMEkUyAed" url="https://app.arcade.software/share/2SmD0N6RcbanMEkUyAed" %}

### Bind your components

**Component Binding** allows the passing of values between components. In this case, we will bind the `Table` and `Filter` components, enabling users to filter Deals by criteria such as `Name`, `Priority`, and `Amount`.

{% @arcade/embed flowId="WeYMccrK3MnPjQeVxhCk" url="https://app.arcade.software/share/WeYMccrK3MnPjQeVxhCk" %}

### Update Deal with a Form component <a href="#3-add-user-management-options-with-a-split-button-component" id="3-add-user-management-options-with-a-split-button-component"></a>

The final component to add is a Form component. This component will allow you to generate [Forms](../../user-guide/design-and-structure/components/form/) automatically based on your Collections fields.

{% @arcade/embed flowId="CSycxxwLOkyFXhQrqax6" url="https://app.arcade.software/share/CSycxxwLOkyFXhQrqax6" %}

Every field in the Form is individually configurable: you can add or remove fields from the Form, alter the field type, rearrange the order of the fields, and change appearance.

{% @arcade/embed flowId="mEmk4at1wRPLQJIEsc7p" url="https://app.arcade.software/share/mEmk4at1wRPLQJIEsc7p" %}

{% content-ref url="display-customers.md" %}
[display-customers.md](display-customers.md)
{% endcontent-ref %}

