# Reading data from API

For instance, you need to make your own API request, just choose `Make an HTTP request` as an operation. Let's look at an example of how to get a list of transactions. We are going to display a list of transactions in the table component with the Stripe API (you can use any API).&#x20;

### Make an API request using API Builder

1\. Go to the Component Settings then `Add Data Resource`

![](../../.gitbook/assets/GIF107.gif)

2\. Select a resource then choose collection as `Make an HTTP request`

![](../../.gitbook/assets/GIF108.gif)

### Pass API parameters

Now you are in API Query Builder. Specify `endpoint` and add new `customer` parameter (to return charges for the customer specified by this customer ID)

![](../../.gitbook/assets/GIF109.gif)

### Use tokens on your API request

When you create a new parameter it becomes available as tokens. You can set a value for the parameter to request a list of customer's transactions.

![](../../.gitbook/assets/GIF110.gif)

### Transform your response

To transform the response, use the `Response Nested Keys` to specify the result of your request:

![](../../.gitbook/assets/GIF111.gif)

### Paginate by pages

To paginate by the list of pages specify `cursor pagination` :

1\. Select `Cusror Pagination` as `Pagination`:

![](../../.gitbook/assets/GIF112.gif)

2\. In general, `Cursor pagination` is specified by `next_cursor`, `has_more` parameters. To parse the response we use Javascript notation. You can modify your function's return value by adding a transformer. Use the identifier `data` for the return value and enter any expressions to modify the result, such as add a property or loop over the data set.&#x20;

* `next_cursor` as `data['data'][data['data'].length - 1].id` &#x20;
* `has_more` as`data['has_more']`

![](../../.gitbook/assets/GIF113.gif)

3\. Let's specify the request by providing `Query Params`:

![](../../.gitbook/assets/GIF114.gif)

### Run your request

Simply click `Refresh Data` button to run your request

![](../../.gitbook/assets/GIF115.gif)

{% content-ref url="../../user-guide/data/make-an-http-request.md" %}
[make-an-http-request.md](../../user-guide/data/make-an-http-request.md)
{% endcontent-ref %}
