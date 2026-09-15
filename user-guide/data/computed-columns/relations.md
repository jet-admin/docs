---
description: Create relationships and link rows together.
---

# Relations

Relations can be used in Jet Admin to create relationships between rows, linking together their data across tables.

The related field allows you to represent the relationships between related records by creating links between them. This is particularly helpful when you have multiple tables of related items. For instance, if you have a table of `Customers` and a table of `Companies`, you can use a related field to link each `Customer row` to the `Company` that they work for.

### Single relations

Single relations show a _one-to-one_ relationship. This is where one item relates to one other item.

### Multiple relations <a href="#multiple-relations" id="multiple-relations"></a>

Multiple relations show a _one-to-many_ relationship. This is where one item relates to a list of other items.

### How to create relations in Jet Admin <a href="#how-to-create-relations-in-glide" id="how-to-create-relations-in-glide"></a>

In Jet, you can create relations between values using a **Link to record** column. With this column, you specify the type of relation you want - single or multiple. Your project then applies the relation to the values and tables specified.

### Check for matching values <a href="#check-for-matching-values" id="check-for-matching-values"></a>

Before adding a **Relation** column, you must first check that the values match the columns that will be connected. Items cannot be linked together unless they match.

In this example, each employee in `Contact` has a `Company` they work in.

1. In the `Contact` table, make sure there’s a column for the name of the employee’s `Company`.
2. In the `Company` table, make sure there’s a column for the name of the location that can be tied to the `Contact` table.

### Build single relations <a href="#build-single-relations" id="build-single-relations"></a>

Here we'll show how to simply create a related Company field for each Customer. Each customer has `company_id`, to display and link the company in the Customer table let's specify `link to record`. Follow the steps:

1. Click on the `Company_id` field
2. Click on the `Number`
3. Select the `Link to Record` option
4. Choose the related R**esource**
5. Choose the related **Collection**
6. Choose **ID** for the **Display Field**

{% @arcade/embed flowId="PkoE2rQCX69JW2AfSjYO" url="https://app.arcade.software/share/PkoE2rQCX69JW2AfSjYO" %}

{% hint style="info" %}
Related field and Display field are set automatically under the context but you can change these values.
{% endhint %}

### Multiple relations <a href="#build-multiple-relations" id="build-multiple-relations"></a>

One record in a table might be connected to many records in another table. For example, I might have a table with my customers and another table with my sales data, and each customer might have multiple orders.

With Jet Admin, you can use this kind of connection to display or work with the connected records that you want.

Example: Create a table that will show all the properties from the landlord selected in the landlord's table.

1. Select the **resource** with the records you want to display. In this case, the table will be with the property's records.
2. Go to the **Data** section
3. Add a filter to the table. You can do this when adding the table, or afterward in the table menu.
4. Choose the related fields and the method of filtering. In this case, the field will be _Landlord ID,_ and the method, _Landlord ID equals_.&#x20;
5. Click on the `Formula` icon, to specify the filter
6. Select the component and field that you want to use to filter. In this example, that will be the _ID_ field from the _landlord's_ table.
7. Choose the **Selected Row -> ID**

{% @arcade/embed flowId="1MRXR7LbZBZGDfIzsn2t" url="https://app.arcade.software/share/1MRXR7LbZBZGDfIzsn2t" %}



