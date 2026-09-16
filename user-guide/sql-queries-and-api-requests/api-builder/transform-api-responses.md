---
description: Transform your JSON response
---

# Transform API responses

Transform a response when its structure does not match the fields your component needs. Test the original request first, then compare the transformed output.

## Select the response root

For a response containing a list inside an object:

```json
{"customers":[{"id":1,"full_name":"Ada"},{"id":2,"full_name":"Grace"}]}
```

1. Open **Transform**.
2. Select **customers** as the response root.
3. Preview the result. It should contain two customer records.

{% @arcade/embed url="https://app.arcade.software/share/CXNncl0iKUKIJ3SaRnyU" flowId="CXNncl0iKUKIJ3SaRnyU" %}

## Rename fields with JavaScript

The variable `data` contains the response. For the original JSON object above:

1. Open **Transform → JavaScript Transformation**.
2. Enter this code:

```javascript
return data.customers.map(customer => ({
  id: customer.id,
  name: customer.full_name
}));
```

3. Run the request and inspect the output:

```json
[{"id":1,"name":"Ada"},{"id":2,"name":"Grace"}]
```

4. Test an empty list: `{"customers":[]}` should return `[]`.
5. Save after the preview matches the fields your component needs.

This code expects the original object with a `customers` array. If you already selected that array as the root, inspect the value passed to the transformation and adjust the code accordingly.

{% @arcade/embed url="https://app.arcade.software/share/Ee03QJrhnsvigKOhEqk7" flowId="Ee03QJrhnsvigKOhEqk7" %}

If the API returns an error or a different shape, resolve that before mapping fields. See [Handle API errors](error-handling.md).
