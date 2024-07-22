---
description: Option de correspondance de catalogue.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# FullMatch{#fullmatch}

Option de correspondance de catalogue.

Une entrée de catalogue est spécifiée sous la forme d’une paire `*`rootId`*/ *`imageId`*` dans les requêtes HTTP. Lors de l’analyse, un catalogue est sélectionné si `*`rootId`*` correspond à la valeur `attribute::RootId` du catalogue et l’enregistrement du catalogue est identifié en faisant correspondre `*`imageId`*` à une valeur `catalog::Id`. Si un catalogue est trouvé, mais qu’aucune entrée de catalogue ne correspond à `*`imageId`*`, le serveur peut effectuer l’une des deux opérations suivantes :

Si `attribute::FullMatch` n’est pas défini, le serveur utilise les attributs du catalogue correspondant. Dans ce cas, `*`rootId`*` est remplacé par `attribute::RootPath` (ou `default::RootPath`, s’il n’est pas spécifié dans ce catalogue).

Si `attribute::FullMatch` est défini, le serveur ignore complètement le catalogue, comme si aucun catalogue n’avait été trouvé, et continue à utiliser les attributs de catalogue par défaut. Dans ce cas, `*`rootId`*` reste une partie du chemin (précédé de `default::RootPath`).

## Propriétés {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Indicateur. Définissez cette valeur sur 0 pour le comportement par défaut ou sur 1 pour activer le comportement de correspondance complète.

## Par défaut {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Hérité de `default::FullMatch` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
