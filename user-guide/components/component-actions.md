# Component Actions

Component actions allow you to **push static or dynamic values into UI components**. You can also use formulas or JavaScript to set the value.

To use this action type, choose the "Run component action" from the action type drop-down:

![](../../.gitbook/assets/xncvygv.JPG)

Then choose the UI component you want to run the component action for:

![](../../.gitbook/assets/xdtjcygv.JPG)

From there, you have two options: **Clear value** or **Set value**:

![](../../.gitbook/assets/djxctft.JPG)

**Clear Value** will simply clear the value of the UI component after the action is successfully executed

**Set Value** allows you to put any value into the UI component after the action is executed.

**As an example**, let's assume we want to create a button that sets the date and time in the Date input field to the current date and time. For this, we'll need to reference the `Date` field in the "Run component action" **(1)** and specify what value we want to put into our `Date` field upon the button click **(2)**.

![](../../.gitbook/assets/ntdxbrd.png)

In our example, we want the date to be set to "Today", so we'll use the `NOW()` formula for that

![](../../.gitbook/assets/trnb66.png)

As a result, we get to set the date to "Today" whenever we click a button:

![](../../.gitbook/assets/thdfvt.gif)
