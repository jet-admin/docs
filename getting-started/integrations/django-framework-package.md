---
description: In this section you will learn how to connect Django to Jet Admin
---

# Django

To integrate Jet Admin with your Django project, you need to install the [Jet Bridge](../../jet-bridge-deployment/jet-admin/) package. It will work even with your local application on localhost. Jet Bridge is an open-source plugin available on [GitHub](https://github.com/jet-admin/jet-bridge). It will connect to your database and link Jet Admin with your project.&#x20;

{% content-ref url="../../jet-bridge-deployment/jet-admin/" %}
[jet-admin](../../jet-bridge-deployment/jet-admin/)
{% endcontent-ref %}

This is the quickest way to install **Jet Admin** for Django-based projects. Installed in the same way as most **Django** packages.&#x20;

#### Requirements

* **Python** 3.4+
* **Django** 1.11+
* **localhost** or **web server** with external IP

### Installation

For installation of Django, follow the steps provided in the article.

1\. Download and install the latest version of **Jet Bridge** for **Django**:

```bash
pip install jet-django
```

2\. Add `jet_django` application to the `INSTALLED_APPS` settings inside **settings.py** file (your Django project):

```python
INSTALLED_APPS = (  ...  'jet_django',  ...)
```

3\. Set `JET_PROJECT` and `JET_TOKEN` inside **settings.py** file:

```
JET_PROJECT = '{{your_project_name}}'
JET_TOKEN = '{{your_jet_token}}'
```

Jet Token is automatically generated for each project, you can find it in the settings.

4\. Add a URL pattern to the **urls.py** file. Remember to import the **path** and **include:**

```python
urlpatterns = [  ...  path('jet_api/', include('jet_django.urls')),  ...]
```

If you use **Django < 2.0:**

```python
urlpatterns = [  ...  url(r'^jet_api/', include('jet_django.urls')),  ...]
```

5\. Run your Django server. Change into the outer project directory, if you haven’t already, and run the following command:

```python
py manage.py runserver
```

6\. Finish the installation by opening this link in your browser, where **localhost** is your **Django** HOST and **8000** is its PORT.&#x20;

```http
http://localhost:8000/jet_api/register/
```

{% hint style="info" %}
**Jet Django** package sets **CORS** headers for **/jet\_api/** endpoints. If it conflicts with your **CORS** headers and you want to deal with it yourself, add the following in **settings.py**: \
JET\_CORS\_HEADERS = False
{% endhint %}

{% content-ref url="../../jet-bridge-deployment/jet-admin/common-problems.md" %}
[common-problems.md](../../jet-bridge-deployment/jet-admin/common-problems.md)
{% endcontent-ref %}

