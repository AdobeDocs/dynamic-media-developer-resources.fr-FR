---
description: Chaîne de modification de demande de préfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères « & ».
solution: Experience Manager
title: Modificateur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---

# Modificateur{#modifier}

Chaîne de modification de demande de préfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères « &amp; ».

Permet de modifier de façon persistante des images et de stocker le corps des modèles.

Les commandes de ce champ sont remplacées par les mêmes commandes dans la requête ou le modèle à partir duquel cet enregistrement est référencé, et par les commandes dans `catalog::PostModifier`

Les macros sont autorisées dans `catalog::Modifier`, à condition qu’elles soient définies dans le même catalogue ou dans le catalogue par défaut. Des variables personnalisées peuvent également être utilisées.

## Propriétés {#section-6674388f77d644469371a17e8809c45f}

Chaîne de texte. Facultatif.

## Par défaut {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Aucune

## Voir aussi {#section-7a67803d141b442180c418c1f3cff029}

[catalogue ::P ostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
