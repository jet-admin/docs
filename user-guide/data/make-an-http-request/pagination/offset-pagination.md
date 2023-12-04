---
description: In this section you will learn how to use offset pagination
---

# Offset pagination

If you see the word `offset` in your API docs, this is the style for you. **Hubspot** uses this style. Their docs say:

Some endpoints support a way of paging the dataset, taking an offset and limit as query parameters:

```javascript
https://api.hubapi.com/v1/deals/v1/deal/paged?offset=20&limit=20

```

In this example, in a list of 20 (`total`) singles by the specified deal: from the twentieth (`offset`) deal, retrieve the next 10 (`limit`) deals.

In Jet API Builder that would be set up with these settings:

```javascript
https://api.hubapi.com/v1/deals/v1/deal/paged?offset={{paging.offset}}&limit={{paging.limit}}
```

![](<../../../../.gitbook/assets/image (841).png>)
