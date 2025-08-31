---
description: >-
  The API Builder makes it simple to connect to external APIs, manage
  authentication, and preview responses. You can configure everything manually
  or let AI handle most of the setup for you.
---

# API Builder

### Making an API Request

To start, go to the **Component Settings** and add a new REST API **Data Resource** or choose **Make an HTTP request**. This opens the API Query Builder, where you can define your request method (GET, POST, PUT, DELETE, etc.) and specify the endpoint URL. For example, you might call:

```http
GET https://api.restful-api.dev/objects
```

This serves as the base of your request before adding headers or parameters.

{% @arcade/embed flowId="xoiwsGNj5Y5L4pjLMGSY" url="https://app.arcade.software/share/xoiwsGNj5Y5L4pjLMGSY" %}

### Ask AI to Build Requests

The **Ask AI** feature makes it even easier to set up your API integration. Instead of manually entering every parameter, you can simply paste your endpoint and provide any necessary details, such as authentication tokens or request type. AI will automatically configure the request for you by placing parameters, headers, body content, and other details in the correct sections. You can also use AI later to adjust or update your request whenever requirements change.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Parameters, Headers, and Tokens

Add query parameters under **Query Params** to filter or refine results. Use the **Headers** tab for authentication or custom headers, such as `Authorization` or `Content-Type`. Tokens and placeholders (e.g., `{{token}}`) are supported for secure, dynamic requests.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Transforming the Response

The **Transform** feature lets you reshape the API response before using it. You can select transformations from a dropdown, or write custom JavaScript to make the response to your needs. For example, you might rename fields, extract only the necessary properties, or reformat arrays.&#x20;

{% hint style="info" %}
If you’re unsure how to write the transformation logic, you can ask AI to generate JavaScript snippets that achieve the desired output. This ensures that your data is always returned in the exact structure you need.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Pagination, Filtering, and Sorting

For large datasets, enable **Pagination**. Client-side pagination applies automatically, while server-side supports **Page, Offset, or Cursor** setups. Filters and sorting can also be applied directly in the builder for quick adjustments.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

{% content-ref url="sorting-data.md" %}
[sorting-data.md](sorting-data.md)
{% endcontent-ref %}

{% content-ref url="pagination/" %}
[pagination](pagination/)
{% endcontent-ref %}

{% content-ref url="error-handling.md" %}
[error-handling.md](error-handling.md)
{% endcontent-ref %}

### Running, Previewing, and Saving Requests

Click **Test Request** to run your API call and view results in the **Preview panel**. Here, you can quickly check the data, verify transformations, and confirm that filters or pagination work as expected. Once everything looks good, hit **Save** in the top-right corner to store your request for reuse across components.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
### Best Practices

To get the most out of the API Builder, make use of the AI assistance for building and updating requests, especially when you need to quickly configure multiple headers or body structures. Always configure headers securely using tokens or placeholders, and enable server-side pagination for large datasets to improve performance. Previewing requests before saving helps verify correctness, while transformations ensure your data is always returned in the right format.
{% endhint %}
