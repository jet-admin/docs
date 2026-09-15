---
description: In this section you will learn about Okta SSO
---

# Okta SSO

### 1. Go to SSO Applications

![](<../../../.gitbook/assets/image (303).png>)

### 2. Create a new SSO application

![](<../../../.gitbook/assets/image (754).png>)

### 3. Go to Okta applications and create new SAML Service Provider

![](<../../../.gitbook/assets/image (757).png>)

![](<../../../.gitbook/assets/image (758).png>)

![](<../../../.gitbook/assets/image (759).png>)

### 4. Specify Attributes Statements

![](<../../../.gitbook/assets/image (760).png>)

### 5. Scroll down and open View Setup Instructions to copy Identity Provider Issuer and enter it below

![](<../../../.gitbook/assets/image (761).png>)

![](<../../../.gitbook/assets/image (766).png>)

### 6. Download Identity Provider metadata

![](<../../../.gitbook/assets/image (763).png>)

### 7. Edit metadata and add entityID attribute (Identity Provider Issuer)

![](<../../../.gitbook/assets/image (764).png>)

### 8. Add User assignments

![](<../../../.gitbook/assets/image (765).png>)

### 9. Upload metadata and set ACS url in Okta

![](<../../../.gitbook/assets/image (755).png>)

### 10. You are all set <a href="#10-you-are-all-set" id="10-you-are-all-set"></a>

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.
