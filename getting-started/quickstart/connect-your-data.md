# Connect your Data

Jet allows you to connect and sync with 50+ data sources: business apps (Airtable, Stripe, Zendesk), Data Warehouses, Internal and external REST or GraphQL APIs, and File Storage. Once a [data source](../../user-guide/integrations/) is set up, you can utilize your data to create apps.

This guide focuses on using [Jet Table](../../user-guide/integrations/jet-tables/) as the data source. Jet Table offers a quick and secure method for storing and modifying data specifically for Jet applications. It integrates the robustness of a PostgreSQL database with the user-friendly aspect of a spreadsheet interface, enabling efficient data management.

To insert test data into the Jet Database, first download the following provided CSV files:

* [Deals](https://res.cloudinary.com/djpvkoh3s/raw/upload/v1699733056/csv%20samples/xuh4l4yizbrwktvbxoae.csv)
* [Companies](https://res.cloudinary.com/djpvkoh3s/raw/upload/v1699733056/csv%20samples/oqak5ieur1t4rgvjkwdx.csv)

Once you have downloaded the CSV files, follow the steps:

1. Log in to Jet Admin and create a new project. If you don't have an account, [sign up](https://app.jetadmin.io/register) for free.
2. Create a new project and add Jet Table as your data source, or if you have an existing project, integrate Jet Table by navigating to **Data** > **Add Resource**.
3. Click **Import CSV**&#x20;
4. Select the **Companies** CSV you downloaded
5. Click **Import file**

{% @arcade/embed flowId="mecpHbmAMz6gVq1gjYiH" url="https://app.arcade.software/share/mecpHbmAMz6gVq1gjYiH" %}

6. Follow the same process to import **Deals: Data** > **Jet Tables > Add or Import.**

{% @arcade/embed flowId="OcDA6NlTW7qooOE72OIg" url="https://app.arcade.software/share/OcDA6NlTW7qooOE72OIg" %}

{% content-ref url="set-the-layout.md" %}
[set-the-layout.md](set-the-layout.md)
{% endcontent-ref %}
