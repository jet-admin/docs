---
description: Choose JSON, XML, Text, or Blob to match an endpoint response.
---

# Choose an API response format

Match the response format to the data returned by the endpoint.

| Format | Use for                                      |
| ------ | -------------------------------------------- |
| JSON   | Objects and arrays, such as customer records |
| XML    | Structured XML responses                     |
| Text   | Plain text, logs, or messages                |
| Blob   | Binary responses, such as files              |

## Configure and check the response

1. Test the endpoint and inspect its returned content.
2. Choose the response format matching that content.
3. Preview the result and confirm that the expected values are available.
4. For a JSON list nested inside an object, select its root and map the fields using [Transform API responses](transform-api-responses.md).

<figure><img src="https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FiTqdBE23qjjCQRbfSKkT%2Fimage.png?alt=media&#x26;token=bab07c0b-5a8c-4a14-9120-e2f46ec3184b" alt="API Builder response format options"><figcaption></figcaption></figure>

A response format controls how content is handled. It does not rename fields or select a nested list; those are transformation tasks.
