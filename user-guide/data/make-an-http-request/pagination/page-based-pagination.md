---
description: In this section you will learn how to use page-based pagination
---

# Page-based pagination

If you see the mention of a numerical page number that you increment to get each page, then you are in the right place.

Intercom uses this style of pagination; it looks like this in their docs:

![](<../../../../.gitbook/assets/image (649).png>)

The first page from this endpoint would look like this: `https://api.intercom.io/users?page=0`

```javascript
$ curl https://api.intercom.io/users?page=0 \
-H 'Authorization:Bearer <access_token>' \
-H 'Accept:application/json'
```

In API Builder that would be set up with these settings:

<figure><img src="../../../../.gitbook/assets/image (1) (4) (2).png" alt=""><figcaption></figcaption></figure>
