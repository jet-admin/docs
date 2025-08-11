---
description: An overview of HTTP request
---

# Making API requests

To quickly connect a custom API, use HTTP Request Builder. You can make `GET` request to visualize order data in the Table component or `POST` request to reset a password for a specific user.&#x20;

![](<../../.gitbook/assets/image (847).png>)

Watch the video below on how to get API Builder set up!

{% embed url="https://www.youtube.com/watch?v=MlNuOS2sffQ" %}

There are two options for creating API requests via **Data** or **Visual Builder.**

To open the API Builder from the **Table**, follow the steps:

1. From the **UI Builder,** drag-and-drop **Table** to the Canvas
2. Select  **Rest API as** `Data Source` in Data
3. Select `Make Http request`  as `Collection`

{% @arcade/embed flowId="NpdjzeS0vHShew1gehsJ" url="https://app.arcade.software/share/NpdjzeS0vHShew1gehsJ" %}

### Pass Values to API Builder

To pass Values to **API Builder**, such as `charge` you need to specify **Inputs**. To do it, follow the steps:

1. Add new `Input` field in the **API Builder**
2. Specify the test value
3. Pass the Input value of the key in the column **Value**
4. Click on the `Run` button to **send a request**
5. Click on the Save button to **save it**

{% @arcade/embed flowId="wcqsojYRvW227Z9Zsr5I" url="https://app.arcade.software/share/wcqsojYRvW227Z9Zsr5I" %}

### Response Transformer

Transform JSON API response using a **Visual** or **Javascript Response Transformer.**

{% content-ref url="make-an-http-request/response-transformer.md" %}
[response-transformer.md](make-an-http-request/response-transformer.md)
{% endcontent-ref %}

### Sorting

Apply ascending or descending sorting to fields from your response.

{% content-ref url="make-an-http-request/sorting-data.md" %}
[sorting-data.md](make-an-http-request/sorting-data.md)
{% endcontent-ref %}

### Pagination

APIs like to send data back in pages. By default, you only get 1 page. You will need to ask for more. In your API docs, there should be a section called Pagination.&#x20;

{% content-ref url="make-an-http-request/pagination/" %}
[pagination](make-an-http-request/pagination/)
{% endcontent-ref %}

### Search

The Search feature allows you to search for text, dates, or numbers within all records and fields of the result of a REST API response.

The search feature works automatically on the client side query operations. But to set the search function on server side query operations, you have to add a "search" parameter in the query parameters and pass \{{search\}} as its value.

<div align="left"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>

By applying the Search query parameter, now the search box will filter all data on all rows and columns with the value typed in the search box.

<div align="left"><figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure></div>



