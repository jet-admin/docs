---
description: In this section you will learn about Auth0 SSO OAuth 2.0
---

# Auth0 SSO OAuth 2.0

### 1. Go to SSO Applications

![](<../../../.gitbook/assets/image (814).png>)

### 2. Create a new SSO application

![](<../../../.gitbook/assets/image (809).png>)

### 3. Go to Auth0 applications and create a new Application

![](<../../../.gitbook/assets/image (768).png>)

![](<../../../.gitbook/assets/image (769).png>)

### 4. Copy credentials to Jet Admin

Choose Provider **Auth0OAuth2** on **Jet Admin** and then copy **Domain, Client ID, Client Secret** from **Auth0**. You should also set **Scope** as **openid,profile,email,offline\_access**.

![](<../../../.gitbook/assets/image (810).png>)

![](<../../../.gitbook/assets/image (811).png>)

### 5. Set Allowed Callback URL on Auth0

Copy the **REDIRECT URL** from **Jet Admin** in the **Application parameters** section to **Auth0 Allowed Callback URLs** and click **Save** on both **- Auth0** and **Jet Admin.**

![](<../../../.gitbook/assets/image (812).png>)

![](<../../../.gitbook/assets/image (813).png>)

### 6. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.
