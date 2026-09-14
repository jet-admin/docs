---
description: >-
  Welcome to the new, AI-powered way to create formulas in Jet Admin! This
  feature allows you to build complex formulas simply by describing what you
  want to achieve.
icon: gear-code
---

# Generate Formulas and JavaScript with AI

The primary benefit of using the AI prompter is its speed and intuitive nature. You no longer need to memorize specific function names or syntax. Just type your goal, and the AI will generate the formula for you, streamlining your workflow and making data manipulation more accessible than ever.

### How to Use AI Formulas: A Step-by-Step Guide

Creating a formula with AI is straightforward. The AI assistant translates your text prompt into a valid formula and places it in the formula editor for your review.

Here’s how to do it:

1. Click on **Add Column** and select **Add a Computed Column**.
2. Give your new column a descriptive label.
3. Click on the **Set up with Formula** icon (fx) next to the value field.
4. In the formula editor, you will see a text box labeled **Ask AI to write or update formula**.
5. Type a clear description of the formula you need into the text box.
6. The AI will generate the corresponding formula and place it in the editor.
7. Review the generated formula. You can make edits directly in the editor if needed.
8. Click **Accept** to apply the formula to your column.

<figure><img src=".gitbook/assets/image (985).png" alt=""><figcaption></figcaption></figure>

### Examples of Common Use Cases

The AI prompter can handle the same tasks as the manual formula builder, from simple text manipulation to complex conditional logic. Below are some common examples adapted from our manual guide to showcase the new AI workflow.

#### Combining Text

This is useful when you have separate data fields, like first and last names, that you want to display together in a single column.

* **Goal**: Combine the `first_name` and `last_name` columns into a single "Full Name" column, separated by a space.
* **Example Prompt**: `Combine the first_name and last_name columns with a space in between.`
* **Generated Formula**: `CONCAT(item.first_name, " ", item.last_name)`

{% @arcade/embed flowId="IXNGNRbU1zanky19Qxpx" url="https://app.arcade.software/share/IXNGNRbU1zanky19Qxpx" %}

#### Basic Math Operations

Perform calculations on your numeric data, such as finding a total cost.

* **Goal**: Calculate the total cost by multiplying the values in the `Price` and `Quantity` columns, and then add a dollar sign prefix to the result.
* **Example Prompt**: `Multiply the Price column by the Quantity column and add a dollar sign at the beginning.`
* **Generated Formula**: `CONCAT("$", item.price * item.quantity)`

{% @arcade/embed flowId="LyaeSVfqv764s5H9blmu" url="https://app.arcade.software/share/LyaeSVfqv764s5H9blmu" %}

#### Conditional Logic

Create custom columns whose values change based on logical conditions in other columns. This is perfect for categorizing data, like scoring customer activity.

* **Goal**: Create a "Score" column based on the value in an "Activities" column. If `activities` are less than 280, the score is '50 points'; if less than 400, it's '70 points'; otherwise, it's '100 points'.
* **Example Prompt**: `If the activities column is less than 280, return '50 points'. If it's less than 400, return '70 points'. Otherwise, return '100 points'.`
* **Generated Formula**: `IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

{% @arcade/embed flowId="3e7kfd9HTXjnNh1tKWeI" url="https://app.arcade.software/share/3e7kfd9HTXjnNh1tKWeI" %}

#### Parsing JSON

If you have data stored in a JSON format within a single field, you can easily extract specific key-value pairs into their own dedicated columns.

* **Goal**: From a column named `JSON_data` that contains JSON objects, extract the value associated with the `pricing` key into a new column.
* **Example Prompt**: `From the paymentDetail column, extract the value from the total field.`
* **Generated Formula**: `NUMBER(GET(item.paymentDetail,"total"))`

{% @arcade/embed flowId="8tHRhk7AyQG2yu31GTD1" url="https://app.arcade.software/share/8tHRhk7AyQG2yu31GTD1" %}

{% hint style="info" %}
### Tips for Writing Effective Prompts

To get the best results from the AI formula generator, keep these tips in mind:

* **Be specific and use exact column names.** The AI works best when you reference columns by their actual names (e.g., `first_name`, `total_cost`).
* **Describe the final output.** Instead of telling the AI which function to use, describe the result you want to see. For example, say "Combine first and last names" rather than "Use the CONCAT function".
* **All functions are available.** The AI has access to the full library of General, Logical, Mathematical, and Date & Time functions. You can ask it to perform any task.
{% endhint %}
