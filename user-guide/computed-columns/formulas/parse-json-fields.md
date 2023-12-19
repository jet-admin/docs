---
description: Parse JSON to create new columns with the data you want
---

# Parse JSON Fields

If your dataset has a field that contains data in a JSON format, you can parse that field to display the specific pieces of data you want in new columns. You can do this by creating a new custom field and then passing it a value that references the JSON field.&#x20;

Let's explain this more in-depth by using the following example.

Suppose you have a field that has JSON data like the following:

```javascript
{
  "fields": {
    "pricing": {
      "integerValue": "109"
    },
    "quantity": {
      "integerValue": "98"
    }
  }
}
```

Without changing anything, it will be displayed like this:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2023-03-16 в 10.23.31.png" alt=""><figcaption></figcaption></figure>

#### To parse this data and make it more readable, follow these steps:

1. Edit the data type for the field with your JSON data. It will be _Text_ by default; change it to JSON.\
   Here you can also change how the data in this column is displayed within this field – as either text or as fields.

<figure><img src="../../../.gitbook/assets/Untitled (1).gif" alt=""><figcaption></figcaption></figure>

2. Create a new Computed Field with the data you want
   1. Click _Add computed column_ in the table menu on the right
   2. Pass the correct value to your field:\
      \- Click the _ƒx Formula_ button\
      \- Choose the field from your table that has your JSON data\
      \- Choose the JSON field and value that you need
   3. Give your column an appropriate name
   4. Adjust the data type for your field as necessary

<figure><img src="../../../.gitbook/assets/Untitled (2).gif" alt=""><figcaption></figcaption></figure>

3. (Optional) Hide the field with the JSON data by clicking on the slider next to the field name in the Table menu

<figure><img src="../../../.gitbook/assets/Untitled (3).gif" alt=""><figcaption></figcaption></figure>
