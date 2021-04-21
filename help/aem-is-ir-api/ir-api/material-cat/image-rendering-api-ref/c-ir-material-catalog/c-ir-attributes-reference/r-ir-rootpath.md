---
description: Chemin d’accès racine des données source. Valeur de chaîne de texte. Chemin absolu ou segment de chemin relatif pour le dossier racine pour tous les fichiers de données de vignette, de texture, d’image et ICC référencés par ce catalogue d’images.
solution: Experience Manager
title: RootPath *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# RootPath *{#rootpath}

Chemin d’accès racine des données source. Valeur de chaîne de texte. Chemin absolu ou segment de chemin relatif pour le dossier racine pour tous les fichiers de données de vignette, de texture, d’image et ICC référencés par ce catalogue d’images.

## Propriétés {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Chaîne de texte. Doit être vide, un segment de chemin d’accès valide relatif au paramètre de configuration du serveur de rendu d’images `ir.resourceRootPaths` ou un chemin d’accès de fichier absolu valide. Ne doit pas inclure de délimiteurs d’élément de chemin de début et de fin.

## Par défaut {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Hérité de `default::RootPath` si elle n&#39;est pas définie. S&#39;il est défini mais vide, ne contribue pas au chemin d&#39;accès racine du fichier source.

## Voir aussi {#section-92012cc1ce32448ea977e7e0484857e2}

[catalogue ::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catalogue::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
