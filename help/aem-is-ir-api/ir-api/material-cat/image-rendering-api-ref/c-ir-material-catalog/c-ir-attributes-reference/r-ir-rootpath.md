---
title: RootPath
description: Chemin d’accès racine des données source. Valeur de chaîne de texte. Chemin d’accès absolu ou segment de chemin d’accès relatif au dossier racine pour tous les fichiers de données image, image, image et ICC référencés par ce catalogue d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# RootPath{#rootpath}

Chemin d’accès racine des données source. Valeur de chaîne de texte. Chemin d’accès absolu ou segment de chemin d’accès relatif au dossier racine pour tous les fichiers de données image, image, image et ICC référencés par ce catalogue d’images.

## Propriétés {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Chaîne de texte. Doit être vide, un segment de chemin valide relatif au paramètre de configuration du serveur de rendu d’image `ir.resourceRootPaths`ou un chemin d’accès absolu au fichier valide. Ne doit pas inclure de délimiteurs d’élément de chemin de début et de fin.

## Par défaut {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Hérité de `default::RootPath` si elle n’est pas définie. S’il est défini, mais vide, il ne contribue pas au chemin racine du fichier source.

## Voir aussi {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalogue ::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
