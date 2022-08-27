---
description: >-
  This guide explains how to quickly connect Supabase back-end to an Jet Admin
  front-end.
---

# Supabase

**Supabase** is an open-source Firebase alternative. &#x20;

### Step 1: Set up your Backend on Supabase <a href="#step-1-set-up-your-backend-on-supabase" id="step-1-set-up-your-backend-on-supabase"></a>

* On the [Supabase dashboard](https://app.supabase.com/), click `New project` and set the name to your **Project**

<figure><img src="../../.gitbook/assets/create-project-supabase-01-4d5930cd172cfc466c97c604b3e1e135.png" alt=""><figcaption></figcaption></figure>

* Create a new table by clicking on the Create Table option on the side navigation.
* Supabase provides many ways to add data to the tables, from writing queries to creating schemas using UI to simply uploading CSV files.&#x20;

<figure><img src="../../.gitbook/assets/create-table-supabase-02-28784eb3dee81672533685563971e45b.png" alt=""><figcaption></figcaption></figure>

### Step 2: Connect the database to Jet Admin <a href="#step-2-connect-the-database-to-appsmith" id="step-2-connect-the-database-to-appsmith"></a>

* Note down the database connection information under Project Settings in Supabase.

<figure><img src="../../.gitbook/assets/supabase.jpg" alt=""><figcaption></figcaption></figure>

Choose a PostgreSQL database from the list of available data sources:

![](<../../.gitbook/assets/image (816).png>)

The quickest way to integrate database (**localhost** not valid, use [**Docker**](postgresql-integration/docker-installation.md) **** or [**Python**](postgresql-integration/python-app-installation.md) **** integration instead). We encrypt all data and credentials that go through our servers using an HTTPS connection.

You'll need to fill out the following form:

![](<../../.gitbook/assets/image (818).png>)

| Name               | Description                                                                                                                                                                                           |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Host               | The IP address or hostname (db.example.com) of where your database instance resides. Note, `localhost` and **`127.0.0.1` are not valid!** Make sure it is accessible from these IPs: `95.179.253.121` |
| User               | Username for this database                                                                                                                                                                            |
| Password           | Password for this database                                                                                                                                                                            |
| Database Name      | The name of the database you would like to interact with.                                                                                                                                             |
| Database Port      | Port to connect to. By default PostgreSQL: 5432                                                                                                                                                       |
| PostgreSQL Schema  | Your database schema (`optional`)                                                                                                                                                                     |
| Extra Parameters   | Extra parameters, ex. charset=utf8 (`optional`)                                                                                                                                                       |
