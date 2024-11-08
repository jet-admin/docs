---
description: Load and Query your data collection/record to your page
---

# Load Data (Page Query)

**Load Data** allows you to retrieve data (collection or record) from the [data sources](../../integrations/), [workflow](../../workflow/), or a page component (specify data). Pass variables/parameters, and filter your data. The data can be loaded into components on the current page: such as [charts](https://docs.jetadmin.io/user-guide/design-and-structure/components/charts), [tables](https://docs.jetadmin.io/user-guide/design-and-structure/components/lists/table), [select, ](../components/form/select.md)and [multiple select](../components/form/multiple-select.md) components.&#x20;

**Load Data** is ideal for scenarios where:

* Multiple components utilize a common data source for enhanced page efficiency
* A single component employs numerous collections for data visualization

### Load Data from Collection

1. Click the **`Actions`** button in the top left menu
2. Click the **`Add Query`** button in the **LOAD DATA** section
3. Select **`Get the list of records`** to retrieve a set of records from a data resource
4. Rename your Page Query
5. Select **Load Data** to retrieve the data from the data resources
6. Select **Data resource**
7. Select **Collection**

{% @arcade/embed flowId="0oq1fvHp4DuPMGCadoqO" url="https://app.arcade.software/share/0oq1fvHp4DuPMGCadoqO" %}

### Load Maximum Records

Load maximum records feature allows you to specify the maximum number of records to load on the page to preserve the page performance. The default maximum number is 20 by default. If you leave this option empty, the value will 20.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

</div>

### **Load Data from JSON**

1. Click on the `Load Data` section
2. Choose **Specify Data**

{% @arcade/embed flowId="fZbifEpDYQ1POPzJDnWD" url="https://app.arcade.software/share/fZbifEpDYQ1POPzJDnWD" %}

### **Load Data from Workflow**

1. Click on the `Load Data` section
2. Choose **Specify Data**
3. Click to `Add a Workflow`
4. Click on the **Run Operation**
5. Choose the **Resource**
6. Choose the **Operation**

{% @arcade/embed flowId="45zZ3kHgWFLiVTKvg9PT" url="https://app.arcade.software/share/45zZ3kHgWFLiVTKvg9PT" %}

## Filter loaded data

1. In the **Apply Filters** section, click Add to implement filters statically or dynamically by using a value from other components.&#x20;
2. Choose the column you would like to filter and then decide on the kind of filter you want to use.

In this example, let's filter by ID. Follow the steps:

1. Click on the `Add Filter` button
2. Choose **ID equals**
3. Click on the `Formula` icon
4. Choose the **component**
5. Choose the **Selected Card**
6. Choose **ID**

{% @arcade/embed flowId="RR9fBsG56BWvEZC05Eqw" url="https://app.arcade.software/share/RR9fBsG56BWvEZC05Eqw" %}

