---
description: Detailed review of pages in Jet Admin.
icon: paintbrush
---

# Customizing Pages

Applies to **Classic App Builder**. The retained video demonstrates the earlier Classic interface.

{% embed url="https://www.youtube.com/watch?v=7382TbvzzRs&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=30&ab_channel=JetAdmin" %}

A Page is an interface element that can span across various use cases. Create pages from scratch or generate an initial page, then configure and test its components.

### Create a New page

To create a new page, follow the steps described in the article:

{% content-ref url="create-a-new-page.md" %}
[create-a-new-page.md](create-a-new-page.md)
{% endcontent-ref %}

### Copy the page

To copy the current page, follow the steps described in the article:

{% content-ref url="copy-the-page.md" %}
[copy-the-page.md](copy-the-page.md)
{% endcontent-ref %}

### Customize the page

Once you created a new page, drag and drop any components to the page to succeed with your use cases.

{% content-ref url="customize-the-page.md" %}
[customize-the-page.md](customize-the-page.md)
{% endcontent-ref %}

### Page Values

Page Values allow you to pass data from one page to another.

{% content-ref url="page-values.md" %}
[page-values.md](page-values.md)
{% endcontent-ref %}

### Link pages

To pass a value from one page to another, you need to use the Navigate to page action.

{% content-ref url="link-pages.md" %}
[link-pages.md](link-pages.md)
{% endcontent-ref %}

## Page Queries

Page queries allow you to do queries from your page at once, and then use query results for all of the components on the page. In case, you use one Query for several components, Page Queries helps you to load it once and optimize the page loading.

{% content-ref url="load-data-page-query.md" %}
[load-data-page-query.md](load-data-page-query.md)
{% endcontent-ref %}

## Load Data (Page Query)

**Load Data** allows you to retrieve data (collection or record) from the [data sources](../../../user-guide/data-sources/), [workflow](../../../workflow/overview.md), or a page component (specify data). Pass variables/parameters, and filter your data. The data can be loaded into components on the current page: such as [charts](../components/charts/), [tables](../components/lists/table/), [select, ](../components/form/select.md)and [multiple select](../components/form/multiple-select.md) components.

{% content-ref url="load-data-page-query.md" %}
[load-data-page-query.md](load-data-page-query.md)
{% endcontent-ref %}

## Page Opens Action

**Page Opens Action** fires each time a page is opened to allow you to perform various actions on the page load, such as [Open Modal](../components/modal.md), Send an [HTTP request](../../../user-guide/sql-queries-and-api-requests/make-an-http-request.md), [Run component action](../../actions-and-logic/actions.md), [show a notification](../components/custom-notifications.md) message, Run a [Workflow](../../../workflow/overview.md), or other actions.

{% content-ref url="page-opens-action.md" %}
[page-opens-action.md](page-opens-action.md)
{% endcontent-ref %}

## Home Page

You can set one or more home pages for your app. There are three options for setting a home page: default to the first page in your menu, select a specific page, or set up a workflow to send users to different pages based on conditions.

{% content-ref url="home-page.md" %}
[home-page.md](home-page.md)
{% endcontent-ref %}
