---
description: >-
  Configuring email sending settings in the environment (.env) file is essential
  for enabling email functionality within your application.
---

# Email Sending Configuration

### **Locate and Open the .env File:** <a href="#locate-and-open-the-.env-file" id="locate-and-open-the-.env-file"></a>

Navigate to the directory where the .env file is located and open it for editing. You can use any text editor of your choice. For example:

```bash
cd jet-onpremise
nano .env
```

### **Simple Email Configuration** <a href="#simple-email-configuration" id="simple-email-configuration"></a>

Modify the following parameters with your email server data:

```
EMAIL_FROM=email@example.com
EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=email_host
EMAIL_PORT=email_port
EMAIL_USER=email_username
EMAIL_PASSWORD=email_password
EMAIL_TLS=1
EMAIL_ADMIN=admin_email@example.com
```

{% hint style="warning" %}
Replace`email@example.com`, `email_host`, `email_port`, `email_username`, `email_password`, and `admin_email@example.com` with your actual email server details.
{% endhint %}

### **Advanced Email Configuration (Amazon SES)**

Alternatively, if you're using Amazon SES for email sending, Add the following parameters with your Amazon SES credentials:

```plaintext
AWS_ACCESS_KEY_ID=aws_access_key_id
AWS_SECRET_ACCESS_KEY=aws_secret_access_key
AWS_REGION=aws_region
AWS_SES_HOST=email-smtp.aws_region.amazonaws.com
AWS_SES_PORT=465
AWS_SES_USER_GROUP=ses_user_group
```

{% hint style="warning" %}
Replace `aws_access_key_id`, `aws_secret_access_key`, `aws_region`, and `ses_user_group` with your actual Amazon SES credentials and region.
{% endhint %}
