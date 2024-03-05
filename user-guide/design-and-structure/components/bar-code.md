# Bar Code

Bar code component allows you to dynamically display any value as a QR code.

## How to add a static Bar Code

Drag and drop Bar Code component onto page and fill it with any value, such as URL.

{% @arcade/embed flowId="qEIZ7OjvAPCTHT7arAtg" url="https://app.arcade.software/share/qEIZ7OjvAPCTHT7arAtg" %}

## Bar Code component settings

<figure><img src="../../../.gitbook/assets/image (936).png" alt=""><figcaption><p>Bar code settings</p></figcaption></figure>

* Component name
* General tab
  * [Format](bar-code.md#bar-code-formats)
  * Value
  * "Display code text" toggle
  * Fill Color
  * Background color
* Display tab
  * Conditional visibility
  * Spacing

### Bar code formats

List of supported bar code formats:

* CODE128 auto
* CODE128 A
* CODE128 B
* CODE123 C
* EAN13
* EAN8
* EAN5
* EAN2
* UPC
* CODE39
* ITF14
* ITF
* MSI
* MSI10
* MSI11
* MSI1010
* MSI1110
* Pharmacode
* Codabar

## How to pass values to Bar Code component

You can [pass any value](layouts/modal/passing-parameters.md) to the component and it will output it as Bar Code.

Let's make an example of displaying SKU as a bar code, referencing the sku from selected row on a table.

You will need:

1. A table with SKU
2. Bar code component

### A table with SKU

Any [table](lists/table/) that has SKU as one of the columns will do.

<figure><img src="../../../.gitbook/assets/image (937).png" alt=""><figcaption><p>Table with products as an example</p></figcaption></figure>



### Bar Code and value formula

Add the QR Component anywhere on the page and click on _"Fx"_ button to start typing in your formula. It should have this syntax:

<pre><code><strong>%component_to_reference%.selected_item.%value%
</strong></code></pre>

{% hint style="info" %}
In this example you won't have to type in formula at all, you can just click on the appropriate value from the side window
{% endhint %}

### Interactive guide with example

{% @arcade/embed flowId="sKAdeMwWIqlAvUKzHpLR" url="https://app.arcade.software/share/sKAdeMwWIqlAvUKzHpLR" %}
