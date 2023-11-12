# Configure Data

In Data, you can set up field types (Number, Text, Select, Date, Rating), define [Relations](../../user-guide/computed-columns/relations.md) between tables, [pull record contents](../../user-guide/data/computed-columns/lookup-column.md) from one linked record into another, [perform a calculation on Relation](../../user-guide/data/computed-columns/rollup-column.md), or [calculate the values](../../user-guide/formulas.md).

Next, let's set up the field type for the **Priority** field. We will configure it as a **Select** type with predefined options: `High`, `Medium`, and `Low`.

{% @arcade/embed flowId="wVznrrHS98pka8fvLcPp" url="https://app.arcade.software/share/wVznrrHS98pka8fvLcPp" %}

Use the Link to **Record** field type to establish a relationship between Deals and Companies. This will enable you to link these two tables, effectively associating specific deals with respective companies.

{% @arcade/embed flowId="f9bvhXrjPJarXzwB1bsq" url="https://app.arcade.software/share/f9bvhXrjPJarXzwB1bsq" %}

Once you've established a Relation using the **Link to Record** field type, you can pull record contents from one linked record into another, and you can perform calculations on this Relation, enabling more complex data manipulations and analyses based on the interconnected data.

{% @arcade/embed flowId="bfEhFWmRJsRH59Mk0jLj" url="https://app.arcade.software/share/bfEhFWmRJsRH59Mk0jLj" %}
