---
description: Suffixe de fichier image par défaut. Ajouté à la valeur du champ Chemin d’accès au catalogue (ou chemin d’accès au catalogue) si le chemin d’accès n’inclut pas de suffixe de fichier
seo-description: Suffixe de fichier image par défaut. Ajouté à la valeur du champ Chemin d’accès au catalogue (ou chemin d’accès au catalogue) si le chemin d’accès n’inclut pas de suffixe de fichier
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# DefaultExt{#defaultext}

Suffixe de fichier image par défaut. Ajouté à la valeur du champ catalog::Path (ou catalog::MaskPath) si le chemin d’accès n’inclut pas de suffixe de fichier.

Un suffixe de fichier se compose d’un point et d’un ou plusieurs caractères entre la période et la fin de la chaîne. Le suffixe est ajouté au chemin d’accès http, si le chemin d’accès n’est pas résolu pour une entrée de catalogue et si le dernier élément de chemin d’accès n’inclut pas de suffixe de fichier.

## Propriétés {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Chaîne de texte. Doit inclure un caractère de début &#39;.&#39; et un ou plusieurs caractères.

## Par défaut {#section-1194c36ffe0748c5b9ff7d732a506588}

Hérité de `default::DefaultExt` si elle n&#39;est pas définie. S’il est défini mais vide, aucun suffixe par défaut n’est appliqué aux noms d’image lors de l’utilisation de ce catalogue.

## Voir aussi {#section-d7c408b979844643adff8258f500eb7c}

[catalogue ::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalogue::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
