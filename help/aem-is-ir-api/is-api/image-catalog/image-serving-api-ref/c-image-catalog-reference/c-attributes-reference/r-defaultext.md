---
description: Suffixe du fichier image par défaut. Ajouté à la valeur du champ Chemin du catalogue (ou chemin du masque de catalogue) si le chemin n’inclut pas de suffixe de fichier.
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# DefaultExt{#defaultext}

Suffixe du fichier image par défaut. Ajouté à la valeur du champ catalog::Path (ou catalog::MaskPath) si le chemin n’inclut pas de suffixe de fichier.

Un suffixe de fichier se compose d’un point et d’un ou de plusieurs caractères entre le point et la fin de la chaîne. Le suffixe est ajouté au chemin http, si le chemin ne se résout pas à une entrée de catalogue et si le dernier élément de chemin n’inclut pas de suffixe de fichier.

## Propriétés {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Chaîne de texte. Doit inclure un &quot;.&quot; au début et un ou plusieurs caractères.

## Par défaut {#section-1194c36ffe0748c5b9ff7d732a506588}

Hérité de `default::DefaultExt` si elle n’est pas définie. S’il est défini mais vide, aucun suffixe par défaut n’est appliqué aux noms d’image lors de l’utilisation de ce catalogue.

## Voir aussi {#section-d7c408b979844643adff8258f500eb7c}

[catalogue ::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalogue ::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
