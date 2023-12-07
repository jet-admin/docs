---
description: An overview of HTTP request
---

# Making API requests

To quickly connect a custom API use HTTP Request Builder. You can make `GET` request to visualize order data in the Table component or `POST` request to reset a password for a specific user.&#x20;

![](<../../.gitbook/assets/image (847).png>)

Watch the video below on how to get API Builder set up!

{% embed url="https://www.youtube.com/watch?v=MlNuOS2sffQ" %}

### Open API Builder

You can open the API Builder directly from the component simply by selecting the Rest API resource. The API Builder will be opened automatically in case you do not create any collections yet, otherwise, you will need to select Make HTTP Request from the list of collections for your Rest API resource.

{% content-ref url="make-an-http-request/open-api-builder.md" %}
[open-api-builder.md](make-an-http-request/open-api-builder.md)
{% endcontent-ref %}

### Response Transformer

You can transform the data from the response with a Visual Response Transformer.

{% content-ref url="make-an-http-request/response-transformer.md" %}
[response-transformer.md](make-an-http-request/response-transformer.md)
{% endcontent-ref %}

### Sorting data

You can sort all fields by ascending and descending values.

{% content-ref url="make-an-http-request/sorting-data.md" %}
[sorting-data.md](make-an-http-request/sorting-data.md)
{% endcontent-ref %}

### Pagination

APIs like to send data back in pages. By default, you only get 1 page. You will need to ask for more. In your API docs, there should be a section called Pagination.&#x20;

{% content-ref url="make-an-http-request/pagination/" %}
[pagination](make-an-http-request/pagination/)
{% endcontent-ref %}
