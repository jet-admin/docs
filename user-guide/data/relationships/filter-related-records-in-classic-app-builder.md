# Filter related records in Classic App Builder

Show the orders belonging to a selected customer in a second table component. This configures a component filter; it does not create a database relationship.

## Before you start

Add a Customers table and an Orders table to a Classic App Builder page. Orders must contain a customer ID that matches the Customers identifier.

## Configure the filter

1. Select the Orders component and open **Data**.
2. Add a filter on **customer\_id**, using **equals**.
3. Select the **Formula** control for the filter value.
4. Choose the Customers component.
5. Select **Selected Row → ID**.

## Verify

Select customer 1 and confirm that only their orders appear. Select customer 2 and check that the list changes. Test the page with no customer selected and configure the component behavior for that state.

The existing walkthrough below demonstrates the same pattern with landlords and properties:

{% @arcade/embed url="https://app.arcade.software/share/1MRXR7LbZBZGDfIzsn2t" flowId="1MRXR7LbZBZGDfIzsn2t" %}

This display filter is not an access-control rule. Apply the appropriate resource and app permissions separately.
