---
title: CacheValidationPolicy
description: Politique de validation du cache du serveur. Indique à quel moment les entrées du cache côté serveur sont validées.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
TQID: 'https://experienceleague.adobe.com/s7dYUadAD1i1ROqCafEZOa5Tztl3ss2HAXnEsPiRGr8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Politique de validation du cache du serveur. Indique à quel moment les entrées du cache côté serveur sont validées.

Avec la validation basée sur l’expiration, les images sources sont périodiquement vérifiées si elles ont changé. Avec la validation par catalogue, les images sources ne sont vérifiées qu’après la modification de la valeur `catalog::TimeStamp`.

La validation catalogue est recommandée lorsque des catalogues d’images sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les images sont référencées directement, sans utiliser de catalogue d’images.

## Propriétés {#section-650cbddd81a24c3b8b70479248a45dc9}

Énumération. 0 pour sélectionner la validation basée sur l’expiration, 1 pour sélectionner la validation de cache basée sur le catalogue.

## Par défaut {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Hérité de `default::CacheValidationPolicy` si non défini ou si vide.

## Voir aussi {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
