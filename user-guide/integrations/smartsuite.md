# SmartSuite

### Connecting SmartSuite

[Create a new Project in Jet Admin](https://app.jetadmin.io/) if you don't have one. You can connect to SmartSuite from the data tab on the left menu bar. You'll need to enter a valid [**API Key**, **Account ID**](smartsuite.md#getting-the-api-key-and-account-id), and select the desired [Solution](smartsuite.md#selecting-smartsuite-solution).

#### Creating a new resource

{% @arcade/embed flowId="T9ql5T43Nwu1kWAseBnb" url="https://app.arcade.software/share/T9ql5T43Nwu1kWAseBnb" %}

#### Getting the API Key and Account ID

Copy the **API Key** and **Account ID** from SmartSuite to Jet Admin.&#x20;

* You can obtain **API KEY** at SmartSuite: User Menu -> API Key
*   And the **Account ID** from SmartSuite URL:&#x20;

    https://app.smartsuite.com/\[ACCOUNT\_ID]/home

{% @arcade/embed flowId="44lq8v9BDQgy6TF2rXJM" url="https://app.arcade.software/share/44lq8v9BDQgy6TF2rXJM" %}

#### Selecting SmartSuite Solution

After you pasted in your API Key and Account ID, you may select the Solution meant to be used in JetAdmin from the drop-down.

{% @arcade/embed flowId="lVwvRwHAU6GgjaXRiYX0" url="https://app.arcade.software/share/lVwvRwHAU6GgjaXRiYX0" %}

{% hint style="info" %}
You can create separate resources for each of your SmartSuite solutions. Jet Admin doesn't have any limits on the amount of your resources
{% endhint %}

### Choosing operation mode&#x20;

After that, you must choose how you'd like your SmartSuite to be integrated with Jet Admin. You can either connect directly or **sync it** with Jet's internal database to get extended functionality.&#x20;

If you want to be able to **combine your SmartSuite data** with data from other data sources, such as Firebase, Google Sheets, or even REST API within the same tables, you should choose the **"Sync" connection** for Google Sheets. You can learn more about it here:

{% content-ref url="../data-blending.md" %}
[data-blending.md](../data-blending.md)
{% endcontent-ref %}

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>Select between "Sync" and "Direct Connection" operation modes</p></figcaption></figure>

{% hint style="info" %}
You can have separate resources for both operation modes and use them differently for separate components on your page
{% endhint %}
