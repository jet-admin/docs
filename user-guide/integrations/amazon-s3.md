---
description: Amazon Cloud Storage
---

# Amazon S3

In order to be able to use Amazon S3 storage in Jet, you need to set it up. Follow the steps below to successfully integrate S3 with Jet.

### Making a new S3 IAM user

Head over to [IAM](https://console.aws.amazon.com/iam/home), add a new user and call it `jetadmin-uploader`, enable _**programmatic access**_ only.&#x20;

![](<../../.gitbook/assets/testgif111 (4).gif>)

Hit _**next**_ to grant the account permissions. The easiest way is granting full S3 permissions, but if you want, you can further restrict the permissions. You'll need to create a new policy, then attach the policy to the created user.

### Configuring Permissions

{% hint style="info" %}
#### IAM Permissions: best practices

While the simplest way to get JetAdmin working with S3 is to give JetAdmin full S3 access, the best practice is to restrict access to buckets on an as-needed basis.
{% endhint %}

![](<../../.gitbook/assets/testgif111 (1).gif>)

### Configuring CORS

Since we upload directly from your browser, you'll need to configure [CORS](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html). Open up the S3 bucket, click the Permissions tab, and then click CORS configuration, and paste in the following JSON, which will let JetAdmin upload directly into your S3 bucket from the browser.

![](<../../.gitbook/assets/testgif111 (5).gif>)

```javascript
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "HEAD",
            "GET",
            "PUT",
            "POST",
            "DELETE"
        ],
        "AllowedOrigins": [
            "*"
        ],
        "ExposeHeaders": [
            "ETag",
            "x-amz-meta-custom-header"
        ]
    }
]
```

### Bucket Settings

JetAdmin require some level of public access to your buckets or objects within, so you need to customize the individual settings below to connect your bucket with JetAdmin.

![](<../../.gitbook/assets/testgif111 (6).gif>)

{% hint style="info" %}
AWS recommends that you turn on Block all public access, but before applying any of these settings, ensure that your applications will work correctly without public access.
{% endhint %}

### Integrate S3 with Jet

Select Amazon S3 from the list of available storages and enter the `access key` and `secret` generated for your IAM user obtained [here](https://console.aws.amazon.com/iam/home#/users). Jet will automatically get a list of all your buckets and integrate each bucket with Jet.

![](<../../.gitbook/assets/image (780).png>)

Once you have integrated S3 with Jet, you will see a Storage File Viewer that you'll use to access your data.

![](../../.gitbook/assets/GIF197.gif)
