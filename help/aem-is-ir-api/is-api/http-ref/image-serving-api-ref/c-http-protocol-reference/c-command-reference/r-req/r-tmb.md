---
description: Image miniature. Demande les données d’image formatées et dimensionnées à l’aide de critères de vignettes de catalogue.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# tmb{#tmb}

Image miniature. Demande les données d’image formatées et dimensionnées à l’aide de critères de vignettes de catalogue.

`req=tmb`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. Prend en charge toutes les commandes, à l’exception de `fit=`.

Voir [Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La réponse HTTP peut être mise en cache avec le TTL en fonction de `catalog::Expiration`.
