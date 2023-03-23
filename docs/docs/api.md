---
layout: default
title: Meta API
nav_order: 2
description: "Meta Documentation"
permalink: /api
last_modified_date: 2023-03-23T14:00:00+0000
---


### Generazione di un token d'accesso dell'app
Per generare un token d'accesso dell'app, hai bisogno dei seguenti elementi:


```bash
curl -X GET "https://graph.facebook.com/oauth/access_token
  ?client_id={your-app-id}
  &client_secret={your-app-secret}
  &grant_type=client_credentials"
```


Contenuto multimediale su un utente di IG
Rappresenta una raccolta di oggetti contenuto multimediale di IG su un utente di IG.

Creazione
POST /{ig-user-id}/media

Consente di creare un contenitore di IG di immagini, video, carosello o reel da usare nella procedura di pubblicazione dei post. Per la procedura completa di pubblicazione, consulta la guida alla pubblicazione dei contenuti.
Limitazioni

### Contenitori immagini
```bash
POST https://graph.facebook.com/{api-version}/{ig-user-id}/media
  ?image_url={image-url}
  &is_carousel_item={is-carousel-item}
  &caption={caption}
  &location_id={location-id}
  &user_tags={user-tags}
  &product_tags={product-tags}
  &access_token={access-token}
```

### Contenitori video
```bash
POST https://graph.facebook.com/{api-version}/{ig-user-id}/media
  ?media_type=VIDEO
  &video_url={video-url}
  &is_carousel_item={is-carousel-item}
  &caption={caption}
  &location_id={location-id}
  &thumb_offset={thumb-offset}
  &product_tags={product-tags}
  &access_token={access-token}
```
### Contenitori reel
```bash
POST https://graph.facebook.com/{api-version}/{ig-user-id}/media
?media_type=REELS
&video_url={reel-url}
&caption={caption}
&cover_url={cover-url}
&location_id={location-id}
&thumb_offset={thumb-offset}
&share_to_feed={share-to-feed}
&access_token={access-token}
```

### Contenitori carosello
Solo contenitori carosello. Per creare contenitori di unità carosello, crea al loro posto contenitori di immagini o video (i reel non sono supportati). Consulta Post carosello per la procedura di pubblicazione completa.
```bash 
POST https://graph.facebook.com/{api-version}/{ig-user-id}/media
?media_type={media-type}
&caption={caption}
&location_id={location-id}
&product_tags={product-tags}
&children={children}
&access_token={access-token}
```