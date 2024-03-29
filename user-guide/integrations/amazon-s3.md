---
description: Amazon and compatible S3 Cloud Storage
---

# Amazon S3 and S3 compatible storage

In order to be able to use Amazon S3 or S3 Compatible storage in Jet, you need to set it up. Follow the steps below to successfully integrate S3 with Jet.

## Creating a new S3 IAM user

Head over to [IAM](https://console.aws.amazon.com/iam/home), add a new user and call it `jetadmin-uploader`, enable _**programmatic access**_ only.&#x20;

![](<../../.gitbook/assets/testgif111 (4).gif>)

Hit _**next**_ to grant the account permissions. The easiest way is granting full S3 permissions, but if you want, you can further restrict the permissions. You'll need to create a new policy, then attach the policy to the created user.

## Configuring Permissions

{% hint style="info" %}
#### IAM Permissions: best practices

While the simplest way to get JetAdmin working with S3 is to give JetAdmin full S3 access, the best practice is to restrict access to buckets on an as-needed basis.
{% endhint %}

![](<../../.gitbook/assets/testgif111 (1).gif>)

## Integrate S3 with Jet

The settings vary depending on what provider you are using. We support any S3 compatible storages.

### AWS S3

Select "Amazon S3" from the list of available storages and enter the `access key` and `secret` generated for your IAM user obtained [here](https://console.aws.amazon.com/iam/home#/users). Jet will automatically get a list of all your buckets, but you will have the ability to define which buckets you want to use.

<figure><img src="../../.gitbook/assets/image (942).png" alt=""><figcaption></figcaption></figure>

### S3 Compatible

Select S3 "Compatible" from the list of available storages. You would need to enter the URL endpoint of your S3, as well as the `access key` and `secret`&#x20;

{% hint style="info" %}
The URL endpoint **should not** contain bucket name. If you have URL with bucket name at the beginning - just remove that part.
{% endhint %}

&#x20;Jet will automatically get a list of all your buckets, but you will have the ability to define which buckets you want to use.

<figure><img src="../../.gitbook/assets/image (943).png" alt=""><figcaption></figcaption></figure>

Once you have integrated S3 with Jet, you will see a Storage File Viewer at your resources page for each of your S3 Resources. You can also perform various operations with storage.

{% hint style="info" %}
Please refer to the article "[Operations with storages](https://docs.jetadmin.io/user-guide/design-and-structure/actions#operations-with-storages)" to know more about avaliable operations.
{% endhint %}
