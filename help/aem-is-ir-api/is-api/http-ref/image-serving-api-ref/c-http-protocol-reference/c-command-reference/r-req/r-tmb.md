---
description: Image miniature. Demande les données image formatées et dimensionnées à l’aide de critères de miniature de catalogue.
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

Image miniature. Demande les données image formatées et dimensionnées à l’aide de critères de miniature de catalogue.

`req=tmb`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. Prend en charge toutes les commandes à l’exception de `fit=`.

Voir [Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La réponse HTTP peut être mise en cache avec le TTL sur la base de `catalog::Expiration`.
