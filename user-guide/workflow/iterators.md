# Iterators

Iterators are a powerful tool in Jet Admin, and they can be implemented in both Automations and Workflows. Here are some example use cases for an iterator:

* Send emails with coupons to customers who left positive/negative ratings
* Create a table that updates automatically every hour with a list of active users
* Keep a table updated with items that are in stock at your store or online shop
* Send a Slack message to your team when important data is updated

## Implementing an iterator

Iterators can be created in automations or workflows. You can add automations in the _Automations_ menu on the left, and workflows can be added to components in the _Actions_ menu of a given component. Remember, workflows are activated as actions and can only be edited within the _Actions_ menu of the component they are applied to, whereas automations are more general and good for purposes like sending Slack notifications when data changes.

<figure><img src="../../.gitbook/assets/automations button.png" alt=""><figcaption></figcaption></figure>

Once you've clicked _Add automation_ in the _Automations_ menu or chosen to add a _Run workflow_ action to a component, you will see the automation builder. Choose a trigger for your automation or workflow.

<figure><img src="../../.gitbook/assets/choose trigger.png" alt=""><figcaption></figcaption></figure>

### Add an iterator and create your automation&#x20;

Add an iterator and the steps that you want to iterate over to your automation. You can also add the iterator in later and drag and drop the steps into it.&#x20;

### Example

#### Iterator that iterates over every record of a table and adds info to different tables depending on the rating that the user gave:

<figure><img src="../../.gitbook/assets/automation example.png" alt=""><figcaption></figcaption></figure>

_For this specific example, it is necessary to create empty tables (with the fields that you want) in Jet Tables that records can then be added to._

#### Steps:

1. This automation is run manually, meaning that to run it, it's necessary to go to the automations menu and select _Run automation._
2. The Xano table is accessed using _Get Record List_, which the Iterator will then iterate over.

<figure><img src="../../.gitbook/assets/Get record list.png" alt=""><figcaption></figcaption></figure>

3. The iterator begins, using _Operation Result_ from _Run Operation - Xano._

<figure><img src="../../.gitbook/assets/Frame 444.png" alt=""><figcaption></figcaption></figure>

4. One record of the _Market Sales_ table is selected, then the Yes/No function sorts it. In this example, _Yes_ is if the customer left a rating of higher than or equal to 5, and _No_ is if the rating is lower than 5. \
   _**Note:**_ If you do not see the _Iterator i_n the menu of steps, click _Test Automation_, and then try again.

<figure><img src="../../.gitbook/assets/Frame 445.png" alt=""><figcaption></figcaption></figure>

5. If the user has left a rating of more than 5/10, certain info from the record is added to the table with the information from higher-rated transactions. If not, that info is added to the other table, with the information from lower-rated transactions.\
   In this example, a label of high rating/low rating has also been included, but in this case it is chosen by the user when setting up the automation.\
   _**Note:**_ As before, if certain options are not available in the menu, click _Test Automation_ and try again.

<figure><img src="../../.gitbook/assets/Frame 446.png" alt=""><figcaption></figcaption></figure>

6. Iterator moves on to next record.

**Once you've completed your automation, be sure to click save it!**
