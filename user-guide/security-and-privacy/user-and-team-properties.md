---
description: In this section you will learn about user-specific permissions
---

# User-specific Permissions

The User and Team properties are useful for the scopes feature: they allow you to group users (not teams) and control the data they can see.

### User & Team Properties

To create a property for a Team or User, you need to go into the settings for the specific Team or User in your application. Follow the steps:

1. Click on the **Profile**
2. Go to the `Users and Teams` tab
3. Go to the `Users Tab`
4. **Select the User** you want to edit
5. Fill in **the Department Section** for that user

{% @arcade/embed flowId="gqo1NuHgl2EHwQtJMwl9" url="https://app.arcade.software/share/gqo1NuHgl2EHwQtJMwl9" %}

To add a property for the user, let's do a simple example of adding Status to the users. To build the example, follow the steps:

1. Click on the `Add Property` icon
2. Choose the **Data Type** of the Property
3. Choose `Select`
4. Rename the property to **Status**
5. **Add** values for the Labels: **Active and Not Active**
6. Click on the `Create` button

{% @arcade/embed flowId="LQGSv1So1EK6nva5LlHq" url="https://app.arcade.software/share/LQGSv1So1EK6nva5LlHq" %}

{% hint style="info" %}
Note that it is important to create User & Team Properties with the same key value so that you can refer to this property via formulas for all properties at once.
{% endhint %}

### Hiding components based on User/Team Properties

Now let's look at an example of hiding a component depending on User & Team Properties and implement the condition of hiding a component if User Property has a read-only value.

{% content-ref url="../components-visibility/conditional-visibility.md" %}
[conditional-visibility.md](../components-visibility/conditional-visibility.md)
{% endcontent-ref %}

### Separating data for users

See here how to use this functionality in the Customer Portal to separate data for users.

{% content-ref url="../../videos/build-apps-together/customer-portal.md" %}
[customer-portal.md](../../videos/build-apps-together/customer-portal.md)
{% endcontent-ref %}
