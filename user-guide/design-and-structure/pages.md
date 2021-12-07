---
description: Detailed review of pages in Jet Admin.
---

# Customizing Pages

A Page is an interface element that can span across various use cases. Create pages from scratch or generate an Admin Panel to get your application ready in less than 2 minutes.

### Create a new page

To create a new page, click on Pages icon on the left menu in Builder mode and click the Create new page icon.

![](../../.gitbook/assets/testgif22.gif)

### Copy your page

To copy the current page, click the Duplicate the page icon next to the page settings:

![](../../.gitbook/assets/testgif72.gif)

### Customize your page

Once you created a new page, drag-and-drop any components to the page to succeed with your use cases.

![](../../.gitbook/assets/testgif23.gif)

{% content-ref url="../components/" %}
[components](../components/)
{% endcontent-ref %}

### Page Values

Page Values allow you to pass data from one page to another.&#x20;

{% content-ref url="../parameters/" %}
[parameters](../parameters/)
{% endcontent-ref %}

In case, when you want to build a Detail page for your user with the user info on this page: first name, last name, address, etc. You need to pass the user ID from one page to another. To do this you need to create a page value for this page and pass this ID to another page in [Action](actions.md).&#x20;

### Create page values

To create page value go to the page settings then click **+Add Parameter.**

![](../../.gitbook/assets/testgif24.gif)

### Link pages

In order to pass a value from one page to another, you need to use the Navigate to page action.

![](../../.gitbook/assets/testgif25.gif)
