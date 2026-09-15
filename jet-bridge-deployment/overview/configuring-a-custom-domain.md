---
description: In this section you will learn how to add a Custom Domain to your application
---

# Custom domain

To add a Custom Domain to your application, follow the steps:

1. Proceed to the Preview button on the top right
2. Click on the **Connect Custom Domain**
3. Type a domain that you would like to connect

{% @arcade/embed flowId="5UHkPMMTLacQxHLQlBR8" url="https://app.arcade.software/share/5UHkPMMTLacQxHLQlBR8" %}



### Add CNAME record

Add the following configuration record in your domain DNS settings:

* Type: **CNAME**
* Name (Host/Domain): **www**
* Destination (Target/Value): **app.jetadmin.io**

Click **Add Domain.** Typically, it takes from 5 minutes to 24 hours to update your DNS.

<figure><img src="../../.gitbook/assets/image (1) (3) (1).png" alt=""><figcaption></figcaption></figure>
