---
description: In this section you will learn how to use Response Transformer
---

# Response Transformer

### Visual Response Transformer

You can transform the data from the response with a Visual Response Transformer. To do so, follow the steps:

1. Click on the `Transform` button
2. Choose the Level of the transform

{% @arcade/embed flowId="CXNncl0iKUKIJ3SaRnyU" url="https://app.arcade.software/share/CXNncl0iKUKIJ3SaRnyU" %}

### JavaScript Response Transformer

If you need custom transformation you can use a JavaScript response transformer. `Data` is a JS variable that stores a response to your request. Javascript transformation. To do so, follow the steps:

1. Click on the `Transform` button
2. Choose **JavaScript Transformation**
3. Write your custom script
4. Click on the `Run` button to send a request
5. Click on the `Save` button to save it

{% @arcade/embed flowId="Ee03QJrhnsvigKOhEqk7" url="https://app.arcade.software/share/Ee03QJrhnsvigKOhEqk7" %}

For example, you can use JS functions to parse the data:

```
function getProperties(data) {
    result = {};
    for (var key in data) {
        result[key] =  data[key]['value'];
    }
    return result;
}

function contactMapper(contactData) {
    result = getProperties(contactData['properties']);
    result['dealId'] = contactData['dealId'];
    return result;
}
return  data['deals'].map((x)=>contactMapper(x));
```

