---
title: CacheValidationPolicy
description: Politique de validation du cache du serveur. Indique à quel moment les entrées du cache côté serveur sont validées.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Politique de validation du cache du serveur. Indique à quel moment les entrées du cache côté serveur sont validées.

Avec la validation basée sur l&#39;expiration, les matériaux sources et les vignettes sont périodiquement vérifiés pour voir s&#39;ils ont changé. Avec la validation par catalogue, les images sources ne sont vérifiées qu’après la modification de la valeur `catalog::TimeStamp`.

La validation catalogue est recommandée lorsque des catalogues de matières et de vignettes sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les vignettes sont référencées dans les requêtes de rendu d’image directement par chemin d’accès.

## Propriétés {#section-46e13cb341eb442c86e0d8292de23ea0}

Énumération. 0 pour sélectionner la validation basée sur l’expiration. 1 pour sélectionner la validation du cache basée sur le catalogue.

## Par défaut {#section-e09f3af8b6b3497d963199988dc5345d}

Hérité de `default::CacheValidationPolicy` si non défini ou si vide.

## Voir aussi {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
