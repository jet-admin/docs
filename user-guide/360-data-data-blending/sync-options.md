---
description: In this section you will learn about Sync Options
---

# Sync Options

The sync parameters can be changed in the **Sync options** tab. To get there, click the three dots in the top left corner of your data source page:

{% @arcade/embed flowId="Nqylpaze42V2N99aCE19" url="https://app.arcade.software/share/Nqylpaze42V2N99aCE19" %}

The syncing consists of two parts: the `Data source` - `Jet tables` connection (referred to as **External updates**) and the `Jet tables` - `Interface` connection (referred to as **Internal updates**). The latter pair is syncing in real-time while the former one's syncing interval can be changed

{% hint style="danger" %}
At the moment, the external updates interval can only be set on the side of Jet Admin, so if you need to change it, reach out to client support
{% endhint %}

In your Data Source page, you can:

* View the **status** (could be <mark style="color:green;">active</mark> or <mark style="color:yellow;">paused</mark>) (1)
* Control the sync: **pause it (2)** or perform a **manual sync** - Sync now (3)

<figure><img src="../../.gitbook/assets/Screenshot 2024-12-26 163715.png" alt=""><figcaption></figcaption></figure>

The last **sync date and time** are displayed along with the sync status:

<figure><img src="../../.gitbook/assets/time.png" alt=""><figcaption></figcaption></figure>

To View Sync Events, follow the steps:

1. Click on the `More` icon
2. Click on the `View Sync Events` button
3. Click on the `More` button

{% @arcade/embed flowId="d5jg7wZ7Ubdzaj91ffn7" url="https://app.arcade.software/share/d5jg7wZ7Ubdzaj91ffn7" %}

To learn more about using SQL queries in Jet Admin, please refer to this page:

{% content-ref url="../../getting-started/part-2-intermediate/reading-data-from-sql-1.md" %}
[reading-data-from-sql-1.md](../../getting-started/part-2-intermediate/reading-data-from-sql-1.md)
{% endcontent-ref %}
