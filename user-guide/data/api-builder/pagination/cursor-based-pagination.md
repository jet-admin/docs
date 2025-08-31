---
description: In this section you will learn how to use cursor-based pagination
---

# Cursor based pagination

Sometimes APIs use something that looks weird for their pagination. Each call may return a cursor key to use to get the next page. Something like _"_`nextPageCursor": "<cursor_key>"` or ID as the next cursor (Stripe API) `"next cursor" : data['data'][data['data'].length - 1].id`

For instance, **Stripe** sends back a URL as well as a cursor (object ID) to use to get the next page. Their docs show this:

![](<../../../../.gitbook/assets/image (648).png>)

You can send this in two ways. Either use the cursor or use the full URL. If you use the cursor, you need to send it in a parameter.

For instance, Stripe API in Jet API Builder that would be set up with these settings:

```javascript
https://api.stripe.com/v1/customers?limit={{paging.limit}}&starting_after={{paging.cursor_next}}&ending_before={{paging.cursor_prev}}
```

<figure><img src="../../../../.gitbook/assets/image (980).png" alt=""><figcaption></figcaption></figure>
