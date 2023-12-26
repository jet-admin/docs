---
description: In this section you will learn about Maps
---

# Map

### Map component

The map component allows you to view and interact with data that has geographical values:

![](<../../../.gitbook/assets/image (687).png>)

### Map data settings

Once you set up your data you need to configure the Location fields.

![](<../../../.gitbook/assets/image (662).png>)

To add a Map to your page, follow the steps:

1. Drag and Drop the **Map** component to the page
2. Specify the **Data source**
3. Specify the **Latitude** and **Longitude** field

{% @arcade/embed flowId="9iL3PwbEezxKaq3DPuys" url="https://app.arcade.software/share/9iL3PwbEezxKaq3DPuys" %}

To do this, you must choose how to set the Location Storage: Latitude/Longitude fields (source data for latitude and longitude) or PostgreSQL format (PostgreSQL Geo Field).

Let's build an example like this:

{% @arcade/embed flowId="KmXrVbqBKGybotz5wkWy" url="https://app.arcade.software/share/KmXrVbqBKGybotz5wkWy" %}

Follow the steps:

1. Go to the `Actions` Tab
2. Choose the Card Click
3. Choose Open Modal
4. Specify the Modal
5. Open the Modal
6. Drag and Drop the Details Component to the Modal
7. Specify the Datasource and bind to the Map Component

{% @arcade/embed flowId="VVMueQyDa3NjcE1oIZQV" url="https://app.arcade.software/share/VVMueQyDa3NjcE1oIZQV" %}

More information about Display Settings, Search, and Action can be found in our documentation.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}
