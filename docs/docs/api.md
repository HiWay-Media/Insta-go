---
layout: default
title: Meta API
nav_order: 2
description: "Meta Documentation"
permalink: /api
last_modified_date: 2023-03-23T14:00:00+0000
---


### Generazione di un token d'accesso dell'app
Per generare un token d'accesso dell'app, hai bisogno dei seguenti elementi:


```bash
curl -X GET "https://graph.facebook.com/oauth/access_token
  ?client_id={your-app-id}
  &client_secret={your-app-secret}
  &grant_type=client_credentials"
```