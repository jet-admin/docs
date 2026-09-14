---
description: In this section you will learn about Custom Domain and Transactional Emails
---

# Custom Domain and Transactional Emails

Jet Admin allows you to use a custom domain for your app, as well as to set up and customize emails for User Invitations,  Email Verification, and Password Restore.

Before you can edit email templates or choose your custom _From_ email address (the default _From_ address is no-reply@jetadmin.app), you will need to set up your custom domain.

## Setting up your custom domain

Click on the _Connect Domain_ button and follow the instructions in the window. First, you will choose the domain name that you want people to see when they visit your app (it should be a subdomain in the format app.yourdomain.com). Then, you will see a message with a CNAME record that you will need to add to your domain DNS settings.

<figure><img src="../../../../.gitbook/assets/image (2) (2) (1).png" alt=""><figcaption></figcaption></figure>

## Customizing _From_ email address

To change the email address that users will see when they receive transactional emails and messages from your app, simply click in the _From email address_ text field, and enter the desired email address. Like with the custom domain, you will need to add CNAME records in your DNS settings to send emails using your domain.\
\
You'll see a pop-up with 3 CNAME records that you need to add to your domain settings.

On some websites, the **Name** (Host/Domain) field may also be called **Subdomain**, while the **Destination** (Target/Value) field may be called **Canonical Name**.

<figure><img src="../../../../.gitbook/assets/Screenshot 2023-08-01 at 04.16.18.png" alt=""><figcaption></figcaption></figure>

## Customizing transactional emails

Jet has three types of automatic, transactional emails: Email Verification, Password Restore, and User Invitation. Email verification is to ensure that your user has entered the correct email address, Password Restore is to help users recover access to their account if they forget their password, and User Invitation is for when you use the Invite Users function when sharing your app. These cover the basic functions for user login setup and troubleshooting, and you can customize each email template to suit your specific needs.

<figure><img src="../../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

To customize transactional email templates, click on the edit icon for the email template that you want to edit, and a template editor modal will appear. Here, you can customize the template however you like, and then you simply need to click _Save._

<figure><img src="../../../../.gitbook/assets/image 428.png" alt=""><figcaption></figcaption></figure>
