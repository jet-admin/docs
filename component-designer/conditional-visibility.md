---
description: In this section you will find out how to use Conditional Visibility
---

# Conditional Visibility

**Conditional Visibility** allows dynamic display adjustments of UI components or layers based on specified conditions. This feature is handy when you need UI elements to respond to changes, such as altering the color of a metric indicator depending on whether its value is positive or negative.

To practice the feature, let's build this example:

<figure><img src="../.gitbook/assets/image (919).png" alt="" width="341"><figcaption></figcaption></figure>

Let's go by colors one by one. For building the green part, please follow the steps:

1. Click on the `Add Fill`  button from the **Right Sidebar**
2. Click on the `Color` button to change the color
3. Click on the `Conditional Fill` button
4. From the **Component Parameters** choose the right parameter
5. Set the condition of the parameter > 0

{% @arcade/embed flowId="gBBLppdGIMSj2HFVKhw6" url="https://app.arcade.software/flows/gBBLppdGIMSj2HFVKhw6/edit" %}

For building the red part, please follow the steps:

1. Click on the `Add Fill`  button from the **Right Sidebar** to add the second fill
2. Click on the `Color` button to change the color
3. Click on the `Conditional Fill` button
4. From the **Component Parameters** choose the right parameter
5. Set the condition of the parameter < 0

{% @arcade/embed flowId="nWgVV1ShbSYWilRDbyc3" url="https://app.arcade.software/share/nWgVV1ShbSYWilRDbyc3" %}

#### Component Property Conditional Visibility

Component Property Visibility allows you to apply conditions to Fills, Borders, and Shadows based on conditions.

#### Component Conditional Visibility

Component Conditional Visibility allows you to show/hide the element (text, shapes, images) on the Component Designer.
