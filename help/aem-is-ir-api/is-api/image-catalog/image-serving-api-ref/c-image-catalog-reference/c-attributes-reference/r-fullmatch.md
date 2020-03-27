---
description: Option de correspondance de catalogue.
seo-description: Option de correspondance de catalogue.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

Option de correspondance de catalogue.

Une entrée de catalogue est spécifiée en tant que paire ` *``*/ *`rootImageId`*` dans les requêtes HTTP. Lors de l’analyse, un catalogue est sélectionné si ` *`rootId`*` correspond à la `attribute::RootId` valeur du catalogue et que l’enregistrement du catalogue est identifié en faisant correspondre ` *`imageId`*` à une `catalog::Id` valeur. Si un catalogue est trouvé, mais qu’aucune entrée de catalogue ne correspond à ` *`imageId`*`, le serveur peut effectuer l’une des deux opérations suivantes :

Si `attribute::FullMatch` n’est pas défini, le serveur utilise les attributs du catalogue correspondant. Dans ce cas, ` *`rootId`*` est remplacé par `attribute::RootPath` (ou `default::RootPath`, s’il n’est pas spécifié dans ce catalogue).

Si `attribute::FullMatch` est défini, le serveur ignore complètement le catalogue, comme si aucun catalogue n’avait été mis en correspondance, et continue à utiliser les attributs de catalogue par défaut. Dans ce cas, ` *`rootId`*` reste une partie du chemin d’accès (précédé par `default::RootPath`).

## Propriétés {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Drapeau. Définissez sur 0 pour le comportement par défaut ou sur 1 pour activer le comportement avec correspondance complète.

## Par défaut {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Héritée de `default::FullMatch` si non définie ou si vide.

## Voir aussi {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
