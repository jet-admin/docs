# QR Code

QR code component allows you to dynamically display any value as a QR code.

## How to add a static QR Code

Drag and drop QR Code component onto page and fill it with any value, such as URL.

{% @arcade/embed flowId="qHf6RxaHTCjtsHpkwGwg" url="https://app.arcade.software/share/qHf6RxaHTCjtsHpkwGwg" %}

## QR Code component settings

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>QR Code settings</p></figcaption></figure>

* Component name
* General tab
  * Value
  * Fill Color
* Background color
* Display tab
  * Conditional visibility
  * Spacing

## How to pass values to QR Code component

You can [pass any value](layouts/modal/passing-parameters.md) to the component and it will output it as QR Code.

Let's make an example of QR codes for sending emails with subject and body, referencing the email from selected row on a table, and getting subject and body from text inputs.

You will need:

1. [A table with emails](qr-code.md#a-table-with-emails)
2. [Two text inputs for subject and body of an email](qr-code.md#text-inputs)
3. [QR code component with formula as a value](qr-code.md#qr-code-and-value-formula)

### A table with emails

Any [table](lists/table/) that has emails as one of the columns will do.

<figure><img src="../../../.gitbook/assets/image (932).png" alt=""><figcaption><p>Table with customers as an example</p></figcaption></figure>

### Text inputs

Drag and drop two text inputs. You can optionally rename them to "Subject" and "Body" and make the second one to have multiple lines.

<figure><img src="../../../.gitbook/assets/image (934).png" alt=""><figcaption><p>Two text inputs</p></figcaption></figure>

### QR Code and value formula

Add the QR Component anywhere on the page and click on _"Fx"_ button to start typing in your formula. It should have this syntax:

<pre><code><strong>FORMAT(
</strong>"mailto: {0} ?subject= {1} &#x26;body= {2}",
%email_value_here%,
%subject_value_here%,
%body_value_here% 
)
</code></pre>

{% hint style="info" %}
Make sure to change the placeholders to values that reference your page
{% endhint %}

### Interactive guide with example

{% @arcade/embed flowId="UBzkyLluSqFqvOFHccxz" url="https://app.arcade.software/share/UBzkyLluSqFqvOFHccxz" %}

