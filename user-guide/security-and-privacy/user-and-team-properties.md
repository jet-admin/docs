# User-specific Permissions

The User and Team properties are useful for the scopes feature: they allow you to group users (not teams) and control the data they can see.

### User & Team Properties

To create a property for a Team or User, you need to go into the settings for the specific Team or User in your application, as shown below:

![](../../.gitbook/assets/testgif68.gif)

{% hint style="info" %}
Note that it is important to create User & Team Properties with the same key value so that you can refer to this property via formulas for all properties at once.
{% endhint %}

### Hiding components based on User/Team Properties

Now let's look at an example of hiding a component depending on User & Team Properties and implement the condition of hiding a component if User Property has a readonly value.

{% content-ref url="../components-visibility/conditional-visibility.md" %}
[conditional-visibility.md](../components-visibility/conditional-visibility.md)
{% endcontent-ref %}

### Separating data for users

See here how to use this functionality in the Customer Portal to separate data for users.

{% content-ref url="../../videos/build-apps-together/customer-portal.md" %}
[customer-portal.md](../../videos/build-apps-together/customer-portal.md)
{% endcontent-ref %}
