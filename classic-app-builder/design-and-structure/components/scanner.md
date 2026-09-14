# Scanner

A scanner component allows you to scan QR codes and Bar codes.

## How to add a scanner component

Drag and drop scanner component onto page and fill it with any value, such as URL.

{% @arcade/embed flowId="rFE9qmOXOAHj94L8d5j3" url="https://app.arcade.software/share/rFE9qmOXOAHj94L8d5j3" %}

## Scanner component settings

<figure><img src="../../../.gitbook/assets/image (938).png" alt=""><figcaption><p>Scanner settings</p></figcaption></figure>

* Component name
* [General tab](scanner.md#general-tab)
  * "[Enable Scan Initially](scanner.md#enable-scan-initially)" toggle
  * "[Ignore Duplicate Scans](scanner.md#ignore-duplicate-scans)" toggle
  * "[Show scan confirmation](scanner.md#show-scan-confirmation)" toggle
* Display tab
  * Conditional visibility
  * Spacing
* [Actions](scanner.md#actions-tab)
  * [When value scanned](scanner.md#when-value-scanned)

### General tab

Settings to change scanner behavior.

#### Enable Scan Initially

When this toggle is enabled, scanner will try to run when page opens.

#### Ignore Duplicate Scans

When this toggle is enabled, scanner will ignore a scan if it was scanned previously.

#### Show Scan Confirmation

When this toggle is enabled, scanner will prompt user after successful scan whether to use this scan or scan again.

<figure><img src="../../../.gitbook/assets/image (939).png" alt=""><figcaption><p>Scan confirmation</p></figcaption></figure>

### Actions tab

#### When value scanned

Here you can set up actions to be performed after a successful scan.

{% hint style="info" %}
Please refer to [Actions article](../actions.md) to know more on what is possible to do with the scan output
{% endhint %}

## How to output values from scanner component

There's two ways of using the output:

#### Referencing output

You can reference output on a page inside other components.

{% hint style="info" %}
Please refer to [Extract & Pass Values](https://docs.jetadmin.io/user-guide/binding-and-values/parameters) to know more on how to pass values to other components
{% endhint %}

Passing output using actions

You can use actions such as running operations, running workflows, or other.

{% hint style="info" %}
Please refer to [Actions article](../actions.md) to know more on what is possible to do with the scan output
{% endhint %}
