---
description: Creating and managing task workflows within Jet Admin
---

# Approval Workflow

As the company is growing and the roles are diversifying, the need for some sort of task management system for your internally-facing applications is increasing. So we came up with the "Task Queue" feature.

{% embed url="https://youtu.be/BjmAml_w0Fs" %}

### How it works

There are certain actions you wouldn't want your support team to have full authority over as the price for the error is high. In that case, you can create an _approval workflow_.  Such a workflow would help:

* route approval requests to the approver
* provide the approver with information pertinent to the case
* make it a rule that certain actions can only be performed if approved
* optionally, enable communication within the approval process&#x20;

Here's the setting: your customer wants his money back. You scroll through the customer list, find the one to return the money to, and select the transaction to be refunded. Now you press the Refund button to make it happen, but here's an approval workflow baked into this process. Therefore, instead of just sending the charged amount back to the customer's account, pressing the Refund button creates a task yet to be approved. You will be presented with a message informing you of the fact, and once you give your consent to the approval requirement, there's a task in the approval tasks queue.

### Create a new task queue

To start, we need to create a new task queue. To do this, follow the steps:&#x20;

1. Go to the **settings** of the **Button** component
2. Select the `Actions tab`
3. Activate the Approval feature for this button

{% @arcade/embed flowId="W7yFruiDSvPP52U30AS4" url="https://app.arcade.software/share/W7yFruiDSvPP52U30AS4" %}

To add a task Queue, follow the steps:

1. Click on the **Select a Queue** button
2. Click on the `Add New` icon
3. Enter the **name** of the task
4. Set statuses that will represent the stages and outcomes of the workflow: the most common statuses would be "new", "in progress" and "completed".&#x20;
5. Click on the `Add` button to save it!

{% @arcade/embed flowId="qmB5ddpxXbdoBGggMKAP" url="https://app.arcade.software/share/qmB5ddpxXbdoBGggMKAP" %}

### Configure the task queue parameters

You can pass helpful information to the task from the application so that the approver can make a better decision of either approving or rejecting a task.

Technically, every meaningful bit of information can be presented to the approver through a corresponding parameter, such as a `transaction id` or a `customer id`:

![](<../../.gitbook/assets/image (845).png>)

A task queue is being formed, and you can perform that action from a Jet Admin application to the approval queue to require approval from the team leader or whoever you set as the assignee of the task.

### Create an approval task

To create an approval task, follow the steps:

1. Select the task queue that we've created in the previous steps.&#x20;
2. For the "**Task Name**" you can either type a name or use formulas to use the dynamic values from the page.&#x20;
3. "**Initial status**" sets the status that the assignee will see in the task queue list and in the task queue details.&#x20;
4. The initial assignee is the person who should receive this task in their task queue and decide whether to approve or reject the task.
5. "**Status after approval**" is the status that the task will change to after approval. Choose Completed as status after approval.
6. "**Status after reject**" is the status that the task will change to after rejection. Choose In Progress as Status after reject.

{% @arcade/embed flowId="EFRLLMuftK6UfHCHNAE5" url="https://app.arcade.software/share/EFRLLMuftK6UfHCHNAE5" %}

### Pass parameters

The next thing to do is to pass parameters that the assignee will see in the task details before making the decision. Those might be the amount of the transaction to refund, the account status any other value from the page, or a formula. You can add as many parameters as you need.

![](<../../.gitbook/assets/image (846).png>)

{% content-ref url="../parameters/" %}
[parameters](../parameters/)
{% endcontent-ref %}

### Approving and rejecting the tasks

Now, every time a user clicks on the "Refund" button, a task is created and passed over to the task queue feed of the chosen assignee. To see the list of tasks you need to open the collaboration page:

![](../../.gitbook/assets/Безымянный.png)

### Organizing the tasks

You can filter tasks by the assignee and the date as well as by the priority. "Priority" is the attribute of the task set by the assignee to help determine how important the given task is.

![](../../.gitbook/assets/GIF157.gif)

### Managing the tasks

After organizing the tasks the assignee can click on the task and view and change the details of the task. The parameters sent along with the task for the given action will appear in the "Details" section:

![](../../.gitbook/assets/GIF159.gif)

### Approving and rejecting tasks

The final step of the workflow is either approving or rejecting the task. Hitting "Approve" will deploy the action that the task has been created for (in our case the refund) and change the task status. Pressing "Reject" will just change the status of the task.&#x20;

![](../../.gitbook/assets/GIF158.gif)
