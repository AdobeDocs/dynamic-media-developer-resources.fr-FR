---
description: Miniature. Demande les données d’image formatées et dimensionnées à l’aide des critères de miniature de catalogue.
solution: Experience Manager
title: œillet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
TQID: 'https://experienceleague.adobe.com/z4QJcR89OAXysP9RV9tZ05ipva3j0CpJYjIzL0KWCnI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 0%

---

# œillet{#tmb}

Miniature. Demande les données d’image formatées et dimensionnées à l’aide des critères de miniature de catalogue.

`req=tmb`

Le format des données de réponse et le type MIME de la réponse sont déterminés par `fmt=`. Prend en charge toutes les commandes, à l’exception de `fit=`.

Voir [ Mise à l’échelle des miniatures ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

La réponse HTTP peut être mise en cache avec la TTL en fonction de `catalog::Expiration`.
