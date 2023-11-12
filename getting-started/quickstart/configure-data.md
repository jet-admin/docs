# Configure Data

In Data, you can set up field types (Number, Text, Select, Date, Rating), define [Relations](../../user-guide/computed-columns/relations.md) between tables, [pull record contents](../../user-guide/data/computed-columns/lookup-column.md) from one linked record into another, [perform a calculation on Relation](../../user-guide/data/computed-columns/rollup-column.md), or [calculate the values](../../user-guide/formulas.md).

Next, let's set up the field type for the **Priority** field. We will configure it as a **Select** type with predefined options: `High`, `Medium`, and `Low`.

1. Click on **Priority** header in your table to access its settings
2. Choose **Edit field** to modify the field's properties.
3. Select the field type as **Select**. This allows you to create a dropdown menu with predefined options.
4. Click on **Display** to proceed with the visual setup.
5. Add predefined options for the 'Priority' field: `High`, `Medium`, and `Low`.

{% @arcade/embed flowId="wVznrrHS98pka8fvLcPp" url="https://app.arcade.software/share/wVznrrHS98pka8fvLcPp" %}

Use the Link to **Record** field type to establish a relationship between Deals and Companies. This will enable you to link these two tables, effectively associating specific deals with respective companies.

1. Click on **Company id** column in your table to access its settings.
2. Choose **Edit field** to modify the field's properties.
3. Select the field type as **Link to record**. This option allows you to create a link between the current record and another table.
4. Specify the related table by selecting **Company**.

{% @arcade/embed flowId="f9bvhXrjPJarXzwB1bsq" url="https://app.arcade.software/share/f9bvhXrjPJarXzwB1bsq" %}

Once you've established a Relation using the **Link to Record** field type, you can pull record contents from one linked record into another, and you can perform calculations on this Relation, enabling more complex data manipulations and analyses based on the interconnected data.

Next, we will focus on extracting and inserting the **Company logo** into the **Deals** table.

1. Click **+ New Column** on the right-top
2. Select **Lookup related field**
3. Select **Company\_id** > **Logo**
4. Save

{% @arcade/embed flowId="bfEhFWmRJsRH59Mk0jLj" url="https://app.arcade.software/share/bfEhFWmRJsRH59Mk0jLj" %}



{% content-ref url="set-the-layout.md" %}
[set-the-layout.md](set-the-layout.md)
{% endcontent-ref %}
