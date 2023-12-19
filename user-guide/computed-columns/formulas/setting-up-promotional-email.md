---
description: In this section, we will build an example of how to set up promotional email
---

# Setting up promotional email

For an introductory example, we will consider feeding customers' email addresses to promotional emails. Once the user is selected in the Customers table, his or her email should appear in the `Email` field to send a promotional Email with a Marketing tool. We will use Functions as well to create a Promotional Email template. For this purpose, we should be performing the following tasks:

1. Click on the **Value text area** -> `Specify with Formula` icon
2. From the pop-up window, select Landlords table  -> Selected row (the value will pass once you click a row) -> User email. The Value field will be populated with the following expression: `=elements.Customers["0"].selected_item.email`
3. Now we will configure the Subject field using the `CONCAT` function. Click on the **Subject text area** -> `Specify with Formula` icon
4. Let's say we want to select an appropriate value from the Discount dropdown list and have it automatically passed to the Subject field of the promotional email in the following form: "Manuel Allen - 15% discount":`=CONCAT(elements.Customers["0"].selected_item.username, " - ", elements["Discount"].value)`
5. Now, we need to configure the Text Body field. Click on the **Text area** -> `Specify with Formula` icon
6. Using the `CONCAT` the function we will build a template for the email body: `=CONCAT("Hi ", elements.Customers["0"].selected_item.first_name, ", here is your promocode: ACX978DF.")`
7. Now when you select any customer, it will launch a completely automated process to create a promotional email to treat this customer. The only manual job remaining for you will be to select the discount and hit the Send email button:

{% @arcade/embed flowId="ivirzoTwWJqjW1WbJmoG" url="https://app.arcade.software/share/ivirzoTwWJqjW1WbJmoG" %}
