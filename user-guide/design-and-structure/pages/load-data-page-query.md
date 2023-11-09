---
description: Load and Query your data collection/record to your page
---

# Load Data (Page Query)

**Load Data** allows you to retrieve data (collection or record) from the [data sources](../../integrations/), [workflow](../../workflow/), or a page component (specify data). Pass variables/parameters, and filter your data. The data can be loaded into components on the current page: such as [charts](https://docs.jetadmin.io/user-guide/design-and-structure/components/charts), [tables](https://docs.jetadmin.io/user-guide/design-and-structure/components/lists/table), [select, ](../../components/fields/select.md)and [multiple select](../components/form/multiple-select.md) components.&#x20;

**Load Data** is ideal for scenarios where:

* Multiple components utilize a common data source for enhanced page efficiency
* A single component employs numerous collections for data visualization

### Load Data from Collection

<figure><img src="../../../.gitbook/assets/image (894).png" alt=""><figcaption></figcaption></figure>

1. Click **Actions** button in the top left menu
2. Click **Add Query** button in the **LOAD DATA** section
3. Select **Get one record** to retrieve one row from a data resource, or **Get the list of records** to retrieve a set of maximum of 20 records from a data resource
4. Rename your Page Query
5. Select **Load Data** to retrieve the data from the data resources
6. Select **Data resource**
7. Select **Collection**

### **Load Data from Workflow or JSON**

<div align="left">

<figure><img src="../../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

</div>

## Filter loaded data

1. In the **Apply Filters** section, click on **Add** to implement filters either statically or dynamically by using a value from other components.&#x20;
2. Choose the column you would like to filter and then decide on the kind of filter you want to use.

<div align="left" data-full-width="false">

<figure><img src="../../../.gitbook/assets/image (896).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left" data-full-width="true">

<figure><img src="../../../.gitbook/assets/image (899).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
For now the Load Data (page query) feature is limited to retrieve only 20 records per request.
{% endhint %}
