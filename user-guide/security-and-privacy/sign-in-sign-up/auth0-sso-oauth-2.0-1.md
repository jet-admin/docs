# Azure AD SSO OAuth 2.0

### 1. Go to Sign In & Sign Up -> Authentication

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### 2. Create a new External SSO

Specify **Name** and **New members team** for newly created **External SSO**

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

### 3. Go to Azure Active Directory -> App registrations and create new new Application

In **Redirect URI (optional)** section fill the following fields

* Platform: Web
* URL: copy **REDIRECT URL** from **Jet Admin -> External SSO** -> **Application parameters** section**.**

<figure><img src="../../../.gitbook/assets/image (2) (5).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### 4. Copy credentials to Jet Admin

* Copy **Application (client) ID** and **Directory (tenant) ID** from **App Registration** page in **Azure portal** to Jet Admin **External SSO**
* Then open **Certificates & secrets** page, create new **Client secret** and copy it's **Value** to Jet Admin **Client Secret**
* You should also set **Scope** to **openid,profile,email,offline\_access**.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1) (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### 5. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.
