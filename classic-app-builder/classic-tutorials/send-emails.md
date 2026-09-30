---
description: Send emails from a Jet app
---

# 📧 Send Emails

Jet Email allows you to send emails via Action or Workflow/Automations. All emails will be sent through **no-reply@jetadmin.app** (unless you have set up a custom _From_ email address in App Settings).

Use the following guide to set up emails, and specify the next operation:

1. Choose operation -> App built-ins
2. Action -> Send email

![](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FIMQzcs9FhWIwbxOiksV5%2Fimage.png?alt=media\&token=b7ffe8ce-84bd-401f-8f71-782417dfbc60)

3\. Specify inputs:

* to – receiver email (allows only email's format)
* subject – text field to specify the email subject
* text – text field without markups
* text (HTML) – text field with markups

![](https://3448227606-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2F4qO3G2tyPZ2k71tdDIOY%2Fimage.png?alt=media\&token=94c6405c-0dc9-4fab-b86d-1728f63b8ffb)

{% hint style="info" %}
On the **Free plan**, the built-in **Send email** action is limited to **one email per minute**. This applies when the action is called directly or from a workflow. Other plans retain the documented limit of 10 emails per minute. Allow for the applicable limit when testing or running email actions.
{% endhint %}
