---
description: In this section you will learn about Google SSO SAML2
---

# Google SSO SAML2

Setting up **SSO** for your **Jet Admin** project requires your to set up **Custom Domain** for your project first.

### 1. Go to SSO Applications

![](<../../../.gitbook/assets/image (303).png>)

### 2. Create a new SSO application

![](<../../../.gitbook/assets/image (304).png>)

### 3. Open your G Suite SAML Apps and create a new one

G Suite Apps page is located at [https://admin.google.com/u/1/ac/apps](https://admin.google.com/u/1/ac/apps)

![](<../../../.gitbook/assets/image (305).png>)

### 4. Select SETUP MY OWN CUSTOM APP

![](<../../../.gitbook/assets/image (306).png>)

### 5. Download IDP metadata .xml file

![](<../../../.gitbook/assets/image (307).png>)

### 6. Specify application basic information

![](<../../../.gitbook/assets/image (308).png>)

### 7. Set up Jet Admin SSO application and copy ACS URL

Specify **Entity ID** and upload saved **Metadata (.xml)** file from the previous step.\
**Entity ID** should be unique text identifier of your application

**ACS URL** displayed at the bottom of page will be needed on the next step.

![](<../../../.gitbook/assets/image (309).png>)

### 8. Set up G Suite SAML App

Specify **ACS URL** and **Entity ID** entered on the previous step

![](<../../../.gitbook/assets/image (312).png>)

### 9. Set attributes mapping

You should specify 3 attributes to map on Jet Admin user account:

* **Email** should map to **Basic Information - Primary Email**
* **FirstName** should map to **Basic Information - First Name**
* **LastName** should map to **Basic Information - Last Name**

![](<../../../.gitbook/assets/image (310).png>)

### 10. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.

![](<../../../.gitbook/assets/image (311).png>)

![](<../../../.gitbook/assets/image (313).png>)
