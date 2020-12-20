---
description: Image miniature. Demande les données d’image formatées et dimensionnées à l’aide de critères de vignettes de catalogue.
seo-description: Image miniature. Demande les données d’image formatées et dimensionnées à l’aide de critères de vignettes de catalogue.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# tmb{#tmb}

Image miniature. Demande les données d’image formatées et dimensionnées à l’aide de critères de vignettes de catalogue.

`req=tmb`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. Prend en charge toutes les commandes, à l’exception de `fit=`.

Voir [Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La réponse HTTP peut être mise en cache avec le TTL en fonction de `catalog::Expiration`.
