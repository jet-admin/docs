# 🔐 Data Privacy & Security

### **Where is my data stored, and is it secure?**

Yes, your data is secure and is always stored by you, whether that be with your chosen data resources or on your own servers. We provide Jet Bridge that makes our architecture secure. Jet Bridge is a free and ope&#x6E;**-**&#x73;ource app that **generates an API** and proxies the requests to databases and business apps. **We don’t collect, copy, or host your private data on our side. Jet follows best practices to ensure that important data is only accessed by you and your users.** Jet encrypts all data and credentials that go through our servers using an HTTPS connection.\
\
Jet Admin offers you the ability to [use Jet Tables](https://docs.jetadmin.io/user-guide/integrations/jet-tables), which is a PostgreSQL database hosted by Jet. Jet Tables, like other top-tier PostgreSQL databases, uses best practices to keep your data secure.  Using Jet Tables is the only case in which your data would be stored on Jet servers, but there is no difference between the way Jet Admin allows you to access data in Jet Tables and the way that Jet allows you to access your data in other PostgreSQL databases, so your data remains secure, regardless of which databases you choose to use. You can learn more about Jet Tables [here.](https://docs.jetadmin.io/user-guide/integrations/jet-tables)

{% content-ref url="jet-bridge-deployment/cloud.md" %}
[cloud.md](jet-bridge-deployment/cloud.md)
{% endcontent-ref %}

Host Jet Bridge on your servers. You can place it behind your VPN, in your own VPC. We won’t get access to your data, however, you will still receive interfaces updates normally.

{% content-ref url="jet-bridge-deployment/jet-admin/" %}
[jet-admin](jet-bridge-deployment/jet-admin/)
{% endcontent-ref %}

If your infrastructure doesn't have access to the internet, you can use on-premise on your own servers and block all network connections. You can place it behind your VPN, in your own VPC.

{% content-ref url="jet-bridge-deployment/on-premise/" %}
[on-premise](jet-bridge-deployment/on-premise/)
{% endcontent-ref %}

## Built-in Security-Grade Features <a href="#built-in-security-grade-features" id="built-in-security-grade-features"></a>



![](<.gitbook/assets/image (738).png>)

### Incident Recovery <a href="#incident-recovery" id="incident-recovery"></a>

To prevent bad consequences for your business, Jet Admin automatically creates a backup of your interface, so you can always restore it in case of an incident. Simply push the “Recover” button at the top right corner of your screen and select what you would like to backup.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGOKqrFcjeSkw6nnATM%2F-MGOUO-nRbXuxE22JoX4%2Frecover-dark%402x.png?alt=media\&token=0e3f32a9-fb29-4994-90ca-a59867b59763)

### DMZ <a href="#dmz" id="dmz"></a>

Since Jet Admin doesn’t require access to your data, you are free to host your admin’s API under DMZ or VPN network. Once you do that, your admin panel will be separated from your public network, leaving no chance for malicious attacks or remote rooting. This might be on a checklist for some large healthcare and financial companies that can be held liable for clients’ personal information. In most cases though, it is not a necessity.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-LqpSrnI1pd1VctEG1LG%2F-LqpT2hOOG5k1OjEq6wb%2Fhow-it-works-dmz%402x.png?alt=media\&token=95609ba5-139e-4fe6-96e5-d04f0bfc51be)
