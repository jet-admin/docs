# Reading data from API

If you need to make your own API request, simply select **"Make an HTTP request"** as the operation. This allows you to connect to any external API and display the response data using available components, such as tables or charts. Just configure the request method, URL, headers, and any necessary parameters based on your API.

### Make an API request using API Builder

1\. Go to the Component Settings then `Add Data Resource`

2\. Select a resource then choose collection as `Make an HTTP request`

{% @arcade/embed flowId="YsnZSlIwPuBdUzzsLNRz" url="https://app.arcade.software/share/YsnZSlIwPuBdUzzsLNRz" %}

### Pass API parameters

Now you are in API Query Builder. Specify `endpoint` and add any new parameter.

<figure><img src="../../.gitbook/assets/image (970).png" alt=""><figcaption></figcaption></figure>

### Use tokens on your API request

If you need to pass tokens or other important headers, simply navigate to the **Headers** section and add the required key-value pairs. For example: `Authorization`, `Content-Type`, or any custom token headers.

<figure><img src="../../.gitbook/assets/image (971).png" alt=""><figcaption></figcaption></figure>

### Transform your response

To transform the response, use the `Transform` feature to specify the result of your request:

<figure><img src="../../.gitbook/assets/image (972).png" alt=""><figcaption></figcaption></figure>

### Paginate by pages

If you need pagination, simply navigate to the **Pagination** section and choose your preferred type — such as **Client-side** or **Server-side** (Page, Offset, or Cursor Pagination).

* For **Client-side** pagination, filters, sorting, and pagination are applied automatically — no additional configuration needed.
* For **Server-side** pagination, select the appropriate type (Page, Offset, or Cursor) and configure the necessary parameters based on your API’s structure. You can also use a transformer to adjust the response format if needed.<br>

<figure><img src="../../.gitbook/assets/image (974).png" alt=""><figcaption></figcaption></figure>

### Run your request

Simply click `Test Request` button to run your request

<figure><img src="../../.gitbook/assets/image (975).png" alt=""><figcaption></figcaption></figure>

{% content-ref url="../../user-guide/data/make-an-http-request.md" %}
[make-an-http-request.md](../../user-guide/data/make-an-http-request.md)
{% endcontent-ref %}
