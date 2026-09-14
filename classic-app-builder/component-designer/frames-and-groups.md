---
description: Both frame and groups are used to host layers similar to directories
---

# Frames and Groups

### Groups

You can group multiple elements to manage them as a single layer. Its child elements determine the boundaries of a group, and adjusting these elements will automatically update the group's dimensions.&#x20;

Groups adjust their boundaries as child elements are resized or moved. Creating a group is non-destructive, meaning it doesn't permanently merge the layers. You can always ungroup the elements later.

You can create a Group by selecting layers and pressing Ctrl + G or ⌘ + G

Grouping is especially useful for organizing similar items and reducing the number of layers to manage in your design. For instance, if you have several icons that need to remain together, grouping them simplifies their management. Clicking any element within the group selects the entire group, making it easy to move or edit as one unit. To select an individual element within a group, ctrl-click on it.

When you resize a group, its child elements will scale proportionally, similar to vector artwork. If you need to apply constraints to control how elements structured, use a frame with Auto Layout instead.

You can define Auto Layout within a group to adjust the positioning of the child layers, although it will transform the group into a Frame.

You can set up Interactions for the whole group instead of individual layers.

### Frames

You can use more features with Frames compared to groups. They allow you to use Auto Layout, specify resizing behavior, as well as utilize their own fills, borders, and shadows.

You can create a Frame using a tool at the top bar, or selecting layers and pressing ⌘ + Opt + G

{% content-ref url="right-sidebar/auto-layout.md" %}
[auto-layout.md](right-sidebar/auto-layout.md)
{% endcontent-ref %}



