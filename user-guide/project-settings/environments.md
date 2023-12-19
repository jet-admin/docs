---
description: How Environments work in Jet Admin
---

# Environments

Environments allow you to have multiple configurations of your project within Jet Admin. If you want to update the resource, add a new one, change the settings, or alter the UI, you can do it safely in a separate environment, whether it's _staging_ or _dev_, and after the changes are reviewed and approved you can merge this new configuration into the _production_ version. You also can create separate environments to control the updates: test the update on the _staging_ environment and then push it into _production_.

{% embed url="https://youtu.be/E3z8j3tBlbI" %}

### Creating a new Environment

By default, any new project is created in the production environment. To quickly add a new environment you need to&#x20;

1. Click the **Add Environment** button in the project settings&#x20;
2. Click on the **Create** button

{% @arcade/embed flowId="EWULBcH5EZQalg40E8wB" url="https://app.arcade.software/share/EWULBcH5EZQalg40E8wB" %}

Now you have a full copy of your production version where you can change, test, and troubleshoot without affecting the production version of the project.

{% hint style="info" %}
Initially, you’ll find a single default environment, which is named “Production”. Any credentials you’ve already added are kept in the "Production" environment. When you connect your data sources to Jet, it uses only the default environment and not any other one.
{% endhint %}

### Managing Updates

To make sure your users always use a stable version of Jet, you can lock the production version of the project in the Production environment, and set the project version to "Latest" in the staging environment. This will keep the staging version up to date and allow you to test any new updates before approving it for production. To do so, follow the steps:

1. Click on the **Jet Admin Version**
2. From the dropdown menu, **choose the Version and Save**

{% @arcade/embed flowId="HFdlTwmrKBovmdKfdMda" url="https://app.arcade.software/share/HFdlTwmrKBovmdKfdMda" %}

### Merging Environments

Once you've made the changes in the staging or development environment, you can transfer those changes onto the production or any other environment. For that,&#x20;

1. In any environment click **Copy environment**.&#x20;
2. Select the environment you'd like to apply changes from and the environment you'd like to apply those changes for.
3. Click **Copy**

{% @arcade/embed flowId="TdFkxHIv5yRz67odxmNZ" url="https://app.arcade.software/share/TdFkxHIv5yRz67odxmNZ" %}



{% hint style="info" %}
You can rename your environment at any time and set a new color for the environment so that you can easily find out which environment you are in right now. You can also create an unlimited number of environments.
{% endhint %}

### Switching between Environments

Any user who is invited into an existing environment can switch between environments. To do so, follow the steps:

1. Hover your mouse over the project icon (top right)&#x20;
2. Select an environment from the drop-down.

{% @arcade/embed flowId="WdrJmtc0Qy6ptvjedGLY" url="https://app.arcade.software/share/WdrJmtc0Qy6ptvjedGLY" %}

{% hint style="info" %}
A user that is not invited to an environment can only see the default "Production" environment.
{% endhint %}
