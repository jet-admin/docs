---
description: Perform calculations on columns or relations like count, average, and sum.
---

# Rollup Column

{% embed url="https://www.youtube.com/watch?v=HBrF6wAMghA&list=PLSkzi9eq0vBnUGMnwXrRRVo9TXUjZ7uSj&index=22&ab_channel=JetAdmin" %}

The roll-up allows you to perform a calculation on [Relation](../../computed-columns/relations.md). The most basic computation for the rollup is Count.

For example, in the image below we create a rollup column that counts the number of items in the `Properties` column. To do so, follow the steps:

1. Click on `Add New Column` Icon
2. Choose `Rollup-Related Records`
3. Choose `Properties`
4. Select `aggregate properties`
5. Click to **Save** it

{% @arcade/embed flowId="gQzmHDhkawUy8SsIbOu1" url="https://app.arcade.software/share/gQzmHDhkawUy8SsIbOu1" %}

### Column or relation source <a href="#column-or-relation-source" id="column-or-relation-source"></a>

![](<../../../.gitbook/assets/image (3) (2) (2).png>)

### Calculations <a href="#calculations" id="calculations"></a>

The Rollup Column can perform different calculations based on the data it finds in the column or relation you select.

#### Numbers <a href="#numbers" id="numbers"></a>

When performing a rollup on numbers, the Rollup Column can execute various calculations to derive meaningful insights.

* **Sum:** Aggregates the total sum of numbers in the specified column or relation.
* **Average (Mean):** Computes the average of the numbers within the chosen column or relation.
* **Minimum (Min):** Identifies the smallest number in the specified data.
* **Maximum (Max):** Determines the largest number found in the chosen column or relation.

#### Dates <a href="#dates" id="dates"></a>

When dealing with date-related information, the Rollup Column can provide insightful calculations:

* **Earliest Date:** Identifies the earliest date within the selected column or relation.
* **Latest Date:** Determines the most recent date present in the specified data.
* **Time Range:** Calculates the duration or period between the earliest and latest dates.
* **Average Duration:** Computes the average time duration between date values.

#### Boolean <a href="#boolean" id="boolean"></a>

For Boolean data, the Rollup Column can offer meaningful computations:

* **Count of True/False:** Determines the number of true or false value occurrences in the chosen column or relation.

#### Text <a href="#text" id="text"></a>

When working with text-based information, the Rollup Column can be employed for diverse calculations:

* **Concatenation:** Combines text values into a single string, facilitating further analysis.
* **Length of Text:** Measures the character length of each text entry.
