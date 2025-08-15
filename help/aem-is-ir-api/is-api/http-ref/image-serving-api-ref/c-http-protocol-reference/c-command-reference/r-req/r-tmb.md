---
description: Image miniature. Demande des données d’image formatées et dimensionnées selon les critères des miniatures du catalogue.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# tmb{#tmb}

Image miniature. Demande des données d’image formatées et dimensionnées selon les critères des miniatures du catalogue.

`req=tmb`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. Prend en charge toutes les commandes sauf `fit=`.

Voir Mise à [l’échelle](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) des miniatures.

La réponse HTTP peut être mise en cache avec la durée de vie (TTL) basée sur `catalog::Expiration`.
