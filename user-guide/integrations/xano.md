---
description: >-
  This guide explains how to quickly connect Xano back-end to a Jet Admin
  front-end.
---

# Xano

Xano is the fastest way to build a powerful, scalable backend for your app without code.

### 1. Ensure you have API CRUD operations in Xano

In the **Xano API section** create **API Group** and fill it with _Create/Read/Update/Delete_ **API endpoints** for your **Database Tables**.

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

### 2. Mark exported API Endpoints

Fill the description fields of API endpoints you want to use in Jet Admin with the following content:

* _For Get record list API endpoint:_ \
  <mark style="background-color:purple;">Query all</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**TABLE**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">records</mark>&#x20;
* _For Create record API endpoint:_ \
  <mark style="background-color:purple;">Add</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**TABLE**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">record</mark>&#x20;
* _For Delete record API endpoint:_ \
  <mark style="background-color:purple;">Delete</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**TABLE**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">record</mark>&#x20;
* _For Get one record API endpoint:_ \
  <mark style="background-color:purple;">Get</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**TABLE**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">record</mark>&#x20;
* _For Update record API endpoint:_ \
  <mark style="background-color:purple;">Edit</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**TABLE**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">record</mark>

Where **TABLE** is your Xano table name.

{% hint style="info" %}
Only endpoints with the specified descriptions will be imported to **Jet Admin**.
{% endhint %}

### 3. Obtain authentication token (if authentication enabled)

**Xano** has built-in authentication to protect **API endpoins** from unauthorized access, you can learn how to set it up in the video:

{% embed url="https://www.youtube.com/watch?v=TiUl1Z8WDXo" %}

Once authentication endpoint is set up, **generate an Auth Token** for **Jet Admin** integration.&#x20;

{% hint style="warning" %}
Make sure to **set expiration to "0"** in endpoint _Create Authentication Token step_ to make Auth Token permanent.&#x20;
{% endhint %}

<div>

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption><p>Copy authToken value to insert it in Jet Admin.</p></figcaption></figure>

</div>

### 4. Add to Jet Admin

Add **Xano** to an existing project or connect **Xano** as a resource when creating a new project. Copy your **API Group Base URL** and **Auth Token** into the Jet Admin connect the resource form.



<div>

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

</div>
