---
description: >-
  Load Data feature allows you to retrieve a record or a set of data up to 20
  records to use on the current page.
---

# Load Data (Page Query)

**Load Data** allows you to retrieve data from the [resources](../../integrations/), a [workflow](../../workflow/), or a page component (specify data) and set filters depending on the page's different use cases. Then use this data collection as a source for the current page components. such as [charts ](https://docs.jetadmin.io/user-guide/design-and-structure/components/charts), [tables](https://docs.jetadmin.io/user-guide/design-and-structure/components/lists/table), [select ](../../components/fields/select.md)and [multiple select](../components/form/multiple-select.md) components.

### To add a **Load Data** to your page follow the steps below:

1- Click the 'Actions' button in the top left menu;\
2- Click the 'Add Query' button in the 'LOAD DATA' section;\
3- Choose 'Get one record' to retrieve one row from a data resource, or 'Get list of records' to retrieve a set of maximum 20 records from a data resource;\
4- Rename your Page Query dataset;\
5- Choose 'Load Data' to retrieve the data from the data resources;\
6- Choose the needed data resource;\
7- Choose the needed collection.\


<figure><img src="../../../.gitbook/assets/image (894).png" alt=""><figcaption></figcaption></figure>

To load data from a custom [workflow](../../workflow/), choose 'Choose using workflow'. To load data from a specific page component or [variable](../../binding-and-values/temporary-and-stored-variables.md), choose 'Specify Data'.\


<div align="left">

<figure><img src="../../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

</div>

## Filter the Load Data

To apply filters statically or dynamically using a value from other components, click the 'Add' button in the 'Apply Filters' section. Choose the column you need to filter then choose the type of filtering you need to apply.\
\


<div align="left" data-full-width="false">

<figure><img src="../../../.gitbook/assets/image (896).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left" data-full-width="true">

<figure><img src="../../../.gitbook/assets/image (899).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
For now the Load Data (page query) feature is limited to retrieve only 20 records per request.
{% endhint %}
