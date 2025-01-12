---
title: Linking Postgres as a source
sidebar: Docs
showTitle: true
availability:
  free: full
  selfServe: full
  enterprise: full
---

The Postgres connector can link your database tables to PostHog.

To link Postgres:

1. Go to the [data warehouse tab](https://us.posthog.com/data-warehouse) in PostHog
2. Click **Link Source** and select Postgres
3. Enter your database connection details:
    - **Host:** The hostname or IP your database server like `db.example.com` or `192.168.1.100`.
    - **Port:** The port your database server is listening to. The default is `5432`.
    - **Database:** The name of the database you want like `analytics_db`.
    - **User:** The username with the necessary permissions to access the database.
    - **Password:** The password for the user.
    - **Schema:** The schema for your database where your tables are located. The default is `public`.
4. Click **Link**

The data warehouse then starts syncing your Postgres data. You can see details and progress in the [data warehouse settings tab](https://us.posthog.com/data-warehouse/settings).

#### Inbound IP addresses

We use a set of IP addresses to access your Postgres instance. To ensure this connector works, add these IPs to your inbound security rules to enable the data import:

| US | EU |
| --- | --- |
| 44.205.89.55  | 3.75.65.221 |
| 44.208.188.173 | 18.197.246.42 |
| 52.4.194.122 | 3.120.223.253 |