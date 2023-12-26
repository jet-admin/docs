---
description: Combine data from different data sources
---

# 💠 360 Data/Data Blending

{% embed url="https://www.youtube.com/watch?v=l1jrrwlj0eU&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=25&ab_channel=JetAdmin" %}

360 Data allows you to connect and sync more than 30 data sources to your Jet app. Jet syncs your data sources to Jet Tables which allows you to join(merge) data and write **SQL with non-SQL** data sources.&#x20;

You can even layer the above capabilities to transform your data the way you want regardless of where it comes from.

{% hint style="info" %}
**All the data sources** you want to be able to blend from have to be connected through the "Sync connection"
{% endhint %}

## Sync Connection

While connecting a data source, you'll be prompted to choose the type of connection, there could be a **direct connection** or a **sync connection.**

{% content-ref url="360-data-data-blending/sync-connection.md" %}
[sync-connection.md](360-data-data-blending/sync-connection.md)
{% endcontent-ref %}

## Blending the data

To demonstrate how the data blending works, we'll use two data sources: Airtable and Google Sheets, where the former contains the `Order` table and the latter - the `Customers` table. Notice that the `Customer ID` column in the `Orders` table refers to the `ID` in the `Customers` table.

{% content-ref url="360-data-data-blending/blending-the-data.md" %}
[blending-the-data.md](360-data-data-blending/blending-the-data.md)
{% endcontent-ref %}

## Sync options

The sync parameters can be changed in the **Sync options** tab. To get there, click the three dots in the top left corner of your data source page:

{% content-ref url="360-data-data-blending/sync-options.md" %}
[sync-options.md](360-data-data-blending/sync-options.md)
{% endcontent-ref %}
