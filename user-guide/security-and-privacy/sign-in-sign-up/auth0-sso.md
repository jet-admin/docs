# Auth0 SSO SAML2

### 1. Go to SSO Applications

![](<../../../.gitbook/assets/image (303).png>)

### 2. Create a new SSO application

![](<../../../.gitbook/assets/image (767).png>)

### 3. Go to Auth0 applications and create new Application

![](<../../../.gitbook/assets/image (768).png>)

![](<../../../.gitbook/assets/image (769).png>)

### 4. Activate SAML2 Web App

![](<../../../.gitbook/assets/image (770).png>)

### 5. Specify mappings in Settings

![](<../../../.gitbook/assets/image (771).png>)

```javascript
{
  "mappings": {
    "email": "Email",
    "given_name": "FirstName",
    "family_name": "LastName"
  }
}
```

### 6. Download metadata

![](<../../../.gitbook/assets/image (772).png>)

### 7. Upload metadata and set ACS url in Auth0

![](<../../../.gitbook/assets/image (773).png>)

### 8. You are all set <a href="#10-you-are-all-set" id="10-you-are-all-set"></a>

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.
