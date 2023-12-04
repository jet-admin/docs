---
description: In this section you will learn how to apply pagination
---

# Pagination

APIs like to send data back in pages. By default, you only get 1 page. You will need to ask for more. In your API docs, there should be a section called Pagination. To set up Pagination, go to the pagination menu in the API Builder:

<figure><img src="../../../../.gitbook/assets/image (2) (7).png" alt=""><figcaption></figcaption></figure>

There are 3 types of pagination: **page**, **offset**, and **cursor pagination**.

When you choose one of these types, variables will automatically be created that you can use in your query parameters – they will be available immediately available for use in the pop-up menu that appears when you click on a query parameter value or in the URL at the top of the API builder. For example, in the image above, automatically created variables are used as the values for the parameters _page_ and _per\_page._

![](<../../../../.gitbook/assets/image (839).png>)
