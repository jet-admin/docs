---
description: >-
  Connect Google Maps to JetAdmin to search places, calculate distances, get
  directions, and access detailed location data.
---

# Google Maps

With the **Google Maps integration**, JetAdmin can leverage Google’s powerful location-based services directly inside your app and workflows.\
After connecting via your Google API key, you can search for places, retrieve directions, look up detailed place information, calculate routes or distances, and more.\
This is ideal for logistics tools, delivery dashboards, travel apps, or any workflow that relies on geographic data.

#### Steps

1. **Go to Data Settings:**\
   In JetAdmin, open **Data → Add Resource**.
2. **Select Google Maps:**\
   Choose **Google Maps** from the list of available data sources.
3. **Name your resource (optional):**\
   Give your connection a clear name like _Maps API_, _Location Services_, or _Geo Tools_.
4. **Paste your Google API Key:**\
   Enter your Google Maps API key.\
   &#xNAN;_&#x4E;ote: Google Maps services must be enabled in your Google Cloud console (e.g., Places API, Directions API, Distance Matrix API)._
5. **Add Resource:**\
   JetAdmin will validate the key. After successful connection, all Maps-related actions become available for use.

{% @arcade/embed flowId="OFZRT6pw1l2OtJOLC1vQ" url="https://app.arcade.software/share/OFZRT6pw1l2OtJOLC1vQ" %}

{% hint style="info" %}
**Actions Overview**\
Once connected, JetAdmin provides a set of powerful geolocation actions, including:\
• **Search Places:** Find nearby locations or search by name, address, or keywords.\
• **Get Directions:** Retrieve driving, walking, or cycling directions between two points.\
• **Get Place Details:** Get extended information such as address, opening hours, ratings,coordinates, and more.\
• **Calculate Distance:** Calculate travel distance and duration between multiple points.

And many more Google Maps actions are also available depending on the APIs you’ve enabled.
{% endhint %}
