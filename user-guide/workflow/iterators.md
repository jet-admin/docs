---
description: In this section you will learn about Iterators
---

# Iterators

Iterators are a powerful tool in Jet Admin, and they can be implemented in both automation and Workflow. Here are some example use cases for an iterator:

* Send emails with coupons to customers who left positive/negative ratings
* Create a table that updates automatically every hour with a list of active users
* Keep a table updated with items that are in stock at your store or online shop
* Send a Slack message to your team when important data is updated

## Implementing an iterator

Iterators can be created in automation or workflows. You can add automation in the _Automation_ menu on the left, and workflows can be added to components in the _Actions_ menu of a given component. Remember, workflows are activated as actions and can only be edited within the _Actions_ menu of the component they are applied to, whereas automation is more general and good for purposes like sending Slack notifications when data changes.

1. Click on the **Automation icon**
2. Click on the `Add automation`&#x20;
3. Choose a trigger for your automation or workflow

{% @arcade/embed flowId="QP5qx9WJgYAGSaSnoQix" url="https://app.arcade.software/share/QP5qx9WJgYAGSaSnoQix" %}

### Add an iterator and create your automation&#x20;

Add an iterator and the steps that you want to iterate over to your automation. You can also add the iterator later and drag and drop the steps into it.&#x20;

### Example

#### Iterator that iterates over every record of a table and adds info to different tables depending on the rating that the user gave:

<figure><img src="../../.gitbook/assets/automation example.png" alt=""><figcaption></figcaption></figure>

_For this specific example, it is necessary to create empty tables (with the fields that you want) in Jet Tables that records can then be added to._

#### Steps:

1. This automation is run manually, meaning that to run it, it's necessary to go to the automation menu and select _Run automation._
2. The Xano table is accessed using the _Get Record List_, which the Iterator will then iterate over.
3. The iterator begins, using _Operation Result_ from _Run Operation - Xano._
4. One record of the _Market Sales_ table is selected, then the Yes/No function sorts it. In this example, _Yes_ is if the customer left a rating of higher than or equal to 5, and _No_ is if the rating is lower than 5. \
   _**Note:**_ If you do not see the _Iterator i_n the menu of steps, click _Test Automation_, and then try again.
5. If the user has left a rating of more than 5/10, certain info from the record is added to the table with the information from higher-rated transactions. If not, that info is added to the other table, with the information from lower-rated transactions.\
   In this example, a label of high rating/low rating has also been included, but in this case, it is chosen by the user when setting up the automation.\
   _**Note:**_ As before, if certain options are not available in the menu, click _Test Automation_ and try again.
6. Iterator moves on to the next record.
7. **Once you've completed your automation, be sure to click save it!**

<figure><img src="../../.gitbook/assets/Frame 445.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Frame 446.png" alt=""><figcaption></figcaption></figure>
