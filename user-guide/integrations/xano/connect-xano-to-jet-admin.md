# Connect Xano to Jet Admin

[Create a new Project in Jet Admin](https://app.jetadmin.io/) if you don't have one. Choose Xano as a Data Source that you would like to connect.

<figure><img src="https://blog.jetadmin.io/content/images/2023/01/xano2.gif" alt=""><figcaption></figcaption></figure>

Copy **API Group Base URL** from Xano to Jet Admin

<figure><img src="https://images.surferseo.art/3e821f48-dc0f-44eb-b1e1-9e870c3a9a67.jpeg" alt=""><figcaption></figcaption></figure>

In case if you would like to protect **API endpoints** from unauthorized access, you can learn how to set it up in the video and get an **Access token**:

{% embed url="https://www.youtube.com/watch?v=TiUl1Z8WDXo" %}

Once authentication endpoint is set up, **generate an Auth Token** for **Jet Admin** integration.

{% hint style="warning" %}
Make sure to **set expiration to "0"** in endpoint _Create Authentication Token step_ to make Auth Token permanent.&#x20;
{% endhint %}

Copy **Authorization token** to **Authorization header** in Jet Admin.

Next, choose Data Sync, which allows you to do SQL queries, and blend and join data from 30+ data sources.

<figure><img src="https://images.surferseo.art/056b7503-9668-442f-9583-855187f6d9c8.png" alt=""><figcaption></figcaption></figure>

<div>

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/image (27) (2).png" alt=""><figcaption><p>Copy authToken value to insert it in Jet Admin.</p></figcaption></figure>

</div>
