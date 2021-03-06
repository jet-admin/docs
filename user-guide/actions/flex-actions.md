# Custom Actions

### What is a Custom Action?

Sometimes CRUD is just not enough...Resetting a password, blacklisting a user, and refunding an order – these are examples of your team’s integral day-to-day operations, that can be automated with Jet Admin.

A Custom Action is a custom button inside Jet’s interface that allows you to realize your own business logic through an API request to your servers.

### How to set up a Custom Actions?

To run operations on your records or implement any custom business logic on the **backend,** you would have to create **Flex Actions** and run them directly from the **Jet Admin** **interface**. 

_Passing additional parameters to your backend is supported._



### 1. Implement Actions on your backend

It will first ask your **backend** for a list of available actions and then will execute them when you need to. Actions that are connected to specific **collections** will automatically appear in the **Jet Admin** interface. Then, you would have to define your **Flex Action**:

1. Define the list of available actions and their parameters
2. Execute a particular action

You can implement a **Flex Action** using one of the following methods:

1. [Implement REST API method](jet-bridge.md)
2. [Django Jet](jet-django.md)

### 2. Specify your actions in Jet Admin

After you have implemented this **API method** you should specify the **Messages URL** field in your Jet Admin **Project Settings** to finish the integration.

Go to Project Settings -&gt; Flex Actions

![](../../.gitbook/assets/image%20%28169%29.png)

![](../../.gitbook/assets/image%20%2871%29.png)

![](../../.gitbook/assets/image%20%286%29.png)

If you've done everything correctly and **saved** all the changes, the actions you've implemented will appear in the Actions list ready-for-execute.

![](../../.gitbook/assets/image%20%28224%29.png)



### Debug mode

Once you've implemented all custom actions on your backend and specified _Message URL_, you can run these actions to check that they've been implemented correctly. First, select an action from the list of all available actions.

![](../../.gitbook/assets/image%20%28199%29.png)

Specify required parameters. If its a Record action, then you should also specify the Record id.

![](../../.gitbook/assets/image%20%283%29.png)

You can check what **Request headers \(including Authorization header\) and data** will be sent to your **API Method** on action execution and what **Response headers and data** are received by **Jet Admin**. It will allow you to simulate real action requests and quickly test your actions.

![](../../.gitbook/assets/image%20%2828%29.png)



![Record FlexAction example](../../.gitbook/assets/image%20%2858%29.png)

**model\_action** is an action that will be applied to selected users \(for\_instance==True flag\)

| Name | Type | Description |
| :--- | :--- | :--- |
|  model | string | Collection name |
| for\_instance | boolean | Specify whether this action should receive record's primary keys to perform actions on particular items instead of the collection itself |
| bulk | boolean | It allows to execute a single action query with ids separated with comma instead of one query per row |

####  <a id="handling-input-values"></a>

### Handling input values

You can also ask users for some parameters for your action. To do that, you would have to define their description in the **params** key. After that. the parameters form will automatically appear in the **Jet Admin** interface.

**params** field is an array of possible parameters in the following format:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Unique name of action</td>
    </tr>
    <tr>
      <td style="text-align:left">field</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>Type of your field, should be one of the following:</p>
        <ul>
          <li>BooleanField</li>
          <li>TranslatableField</li>
          <li>SelectField</li>
          <li>ForeignKey (required a parameter &#x2013; <b>params, </b>see below)</li>
          <li>DateTimeField</li>
          <li>TimestampField</li>
          <li>DateField</li>
          <li>TimeField</li>
          <li>JSONField</li>
          <li>SqlField</li>
          <li>CodeField</li>
          <li>CharField</li>
          <li>TextField</li>
          <li>IntegerField</li>
          <li>FloatField</li>
          <li>DecimalField</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">params</td>
      <td style="text-align:left">dictionary</td>
      <td style="text-align:left">Additional parameters for fields, such as <b>ForeignKey,</b> require you
        to specify the <b>related_model</b> option</td>
    </tr>
    <tr>
      <td style="text-align:left">required</td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left">(optional) If <code>True</code>, your input field will be set as required
        in the browser. Default is <code>False</code>
      </td>
    </tr>
  </tbody>
</table>

{% code title="flex\_action\_params\_example.py" %}
```python
# Example for requesting paramters from user for action
def get_action_list(params):
    return [
        {
            'name': 'account_transfer',
            'model_action': {
                'model': ['projects;income', 'projects;outcome'],
                'for_instance': False
            },
            'params': [
                {
                    'name': 'account_from',
                    'field': 'ForeignKey',
                    'params': {'related_model': {'model': 'projects;account'}}
                },
                {
                    'name': 'amount_from',
                    'field': 'DecimalField'
                },
                {
                    'name': 'account_to',
                    'field': 'ForeignKey',
                    'params': {'related_model': {'model': 'projects;account'}}
                },
                {
                    'name': 'amount_to',
                    'field': 'DecimalField'
                },
                {
                    'name': 'description',
                    'field': 'TextField',
                    'required': False
                },
                {
                    'name': 'date',
                    'field': 'DateTimeField',
                    'required': False
                }
            ]
        }
    ]
```
{% endcode %}

![Collection FlexAction example](../../.gitbook/assets/image%20%2851%29.png)

![](../../.gitbook/assets/image%20%28113%29.png)

### Responses

The simplest **FlexAction** response contains only one Boolean `result` indicating whether **FlexAction** execution succeeded or not. Response should be a JSON formatted Object \(except  file download response\).

```python
{
    "result": true
}
```

#### Displaying success message

If you want to display custom success message, you can return`message` as a string.

```python
{
    "result": true,
    "message": "User wallet was updated"
}
```

#### Displaying errors

If you want to display some errors to a user, you should include the`errors` Object which can contain general errors or errors of some particular input values. So the keys of such objects should either be equal to one of the input values or for general – `non_field_errors`. Values of this object are an array of strings \(so you can return multiple errors for the same field\). Here is an example:

```python
{
    "result": false,
    "errors": {
        "non_field_errors": [
            "User is inactive",
            "User balance is below zero"
        ],
        "amount": ["Payment amount can't be negative"],
    }
}
```

#### Displaying HTML

If you want to render HTML for a user, you can also generate and return raw HTML which will be displayed in the Jet Admin interface:

```javascript
{
    "result": true,
    "html": "User <strong>wallet</strong> was updated"
}
```

#### Downloading a file

You can return a user file for downloading by sending it in Response Body with the appropriate headers:

```http
Content-Type: application/pdf
Access-Control-Expose-Headers: Content-Disposition
Content-Disposition: attachment; filename=order_dbb5a75e.pdf
```

