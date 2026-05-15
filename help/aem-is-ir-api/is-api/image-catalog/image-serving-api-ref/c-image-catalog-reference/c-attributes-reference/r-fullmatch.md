---
description: Option de correspondance de catalogue.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
TQID: 'https://experienceleague.adobe.com/5eTvORUSVsXHReAaiVMGSizooDQ9Wq--dXrBo0c9C7c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 1%

---

# FullMatch{#fullmatch}

Option de correspondance de catalogue.

Une entrée de catalogue est spécifiée en tant que paire `*`rootId`*/ *`imageId`*` dans les requêtes HTTP. Lors de l’analyse, un catalogue est sélectionné si `*`rootId`*` correspond à la valeur `attribute::RootId` du catalogue et l’enregistrement du catalogue est identifié en faisant correspondre `*`imageId`*` avec une valeur `catalog::Id`. Si un catalogue est trouvé, mais qu’il n’existe aucune entrée de catalogue correspondant à `*`imageId`*`, le serveur peut effectuer l’une des deux opérations suivantes :

Si `attribute::FullMatch` n’est pas défini, le serveur utilise les attributs du catalogue correspondant. Dans ce cas, `*`rootId`*` est remplacé par `attribute::RootPath` (ou `default::RootPath`, s’il n’est pas spécifié dans ce catalogue).

Si `attribute::FullMatch` est défini, le serveur ignore complètement le catalogue, comme si aucun catalogue ne correspondait, et continue à utiliser les attributs de catalogue par défaut. Dans ce cas, `*`rootId`*` reste une partie du chemin d’accès (qui est précédé de `default::RootPath`).

## Propriétés {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Drapeau. Définissez cette valeur sur 0 pour le comportement par défaut ou sur 1 pour activer le comportement de correspondance complète.

## Par défaut {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Hérité de `default::FullMatch` si non défini ou si vide.

## Voir aussi {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
