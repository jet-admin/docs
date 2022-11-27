# Modal

Before we get into the nuances of using a modal in a JetAdmin app, it’s probably worth taking a moment to define what a modal is in the first place.&#x20;

Modals are windows - both large and small - that “pop” onto the screen when an action is taken. Sometimes these come in the form of a warning (e.g. “Are you sure you want to delete that?”) and sometimes they can be in the form of something useful (e.g. clicking a "view details" button and seeing the specifics about an object).&#x20;

Modals allow you to both save space as well as present the right information, at the right time.

![](../../.gitbook/assets/testgif97.gif)

### The basics and properties

To add a modal into your application, find button in the component sidebar on the right and drag in onto the page. It will look just like a normal button at first, so don’t be alarmed. To see the modal in action, click the button. Once you do so, you’ll see the modal window pop up.

![](../../.gitbook/assets/testgif98.gif)

{% hint style="info" %}
An open modal acts as a Page does, meaning that you can drag-and-drop other components into it when it’s open.
{% endhint %}

You can change the width of the modal window and the content will automatically be adjusted:

![](../../.gitbook/assets/testgif99.gif)

Modal windows in Jet Admin have various display styles. You can change it in the modal settings:

![](../../.gitbook/assets/testgif100.gif)

You can also set the title for the modal window in different ways. The title can be a **static** value or a **dynamic** value using formulas (e.g., you want to display Update Product # \{{id\}}).&#x20;

![](../../.gitbook/assets/testgif101.gif)

See here for more details on how to use the formula functionality for dynamic values:

{% content-ref url="../formulas.md" %}
[formulas.md](../formulas.md)
{% endcontent-ref %}

### Open a Modal from a Table

You have a table that displays a list of Products. After clicking on the product row (the selected row) you want to see product details - displayed in modal. To do this, let's set up a Row click action with the **Open Modal** type:

![](../../.gitbook/assets/testgif102.gif)

Next, you can choose a created and configured modal or create a new one:

![](../../.gitbook/assets/testgif103.gif)

Now let's add a Detail component to the Modal window to display detailed information:

![](../../.gitbook/assets/testgif104.gif)

Next, you need to apply filters, namely a data filter on the primary key (in our case it is the product ID). This step is important for the form to display exactly the data you selected in the table (selected row):

![](../../.gitbook/assets/testgif105.gif)

{% hint style="info" %}
Now, when you select a row, the modal window will open with product details.
{% endhint %}

