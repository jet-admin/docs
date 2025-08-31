---
description: >-
  Use the Error Handling section to define custom logic for extracting and
  displaying meaningful messages from failed HTTP responses.
---

# Error Handling

### Purpose

The **Error Message Function** enables you to interpret and return appropriate error messages based on the HTTP response from an external API. This function is evaluated automatically whenever an API call fails, allowing you to present users with more specific, helpful feedback.

{% @arcade/embed flowId="5XUOfkOOOZ8xZVBLw9tF" url="https://app.arcade.software/share/5XUOfkOOOZ8xZVBLw9tF" %}

### Default Error Handling Behavior

Below is the default logic used in the Error Message Function:

```javascript
// Add custom transformation here
if (http.code >= 200 && http.code < 400) {
  // No error if success code
  return null;
} else if (data['message']) {
  // Display error message if available in response
  return data['message'];
} else {
  // Generic error if no message found
  return true;
}

```

#### Explanation:

* **`http.code >= 200 && http.code < 400`**\
  If the HTTP response code indicates success (2xx or 3xx), no error is returned.
* **`data['message']`**\
  If the response contains a message field (e.g., `{ "message": "Invalid credentials" }`), it will be displayed as the error message.
* **`return true`**\
  If no specific message is found, a generic error is triggered.

### Custom Error Handling Examples

You can extend this function to handle specific status codes or error formats depending on your API’s behavior.

Example 1: Handle Unauthorized Access (HTTP 401) with Default Fallback

```javascript
if (http.code === 401) {
  return "Unauthorized access. Please check your API credentials.";
} else if (data['message']) {
  return data['message'];
} else {
  return true;
}

```

Example 2: Handle Rate Limiting (HTTP 429) and Fallback to Default

```javascript
if (http.code === 429) {
  return "Too many requests. Please wait and try again.";
} else if (data['message']) {
  return data['message'];
} else {
  return true;
}

```

### 🛠️ Recommended Template: Combine Custom + Default Logic

You can use the following pattern as a **template** to cover both **specific cases** and **general fallback behavior**:

```javascript
// Custom error handling
if (http.code === 401) {
  return "Unauthorized access. Please log in again.";
}

if (http.code === 429) {
  return "Rate limit exceeded. Try again in a few moments.";
}

// Default behavior fallback
if (http.code >= 200 && http.code < 400) {
  return null;
} else if (data['message']) {
  return data['message'];
} else {
  return true;
}

```

{% hint style="info" %}
Error Handling Best Practices

* Always include the **default logic** at the end to ensure error messages are still shown even if your custom cases don’t apply.
* Start with **specific status codes or header-based conditions** to catch known patterns.
{% endhint %}
