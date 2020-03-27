---
description: Chaîne de modificateur de requête de préfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères "&".
seo-description: Chaîne de modificateur de requête de préfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères "&".
seo-title: Modificateur
solution: Experience Manager
title: Modificateur
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Modificateur{#modifier}

Chaîne de modificateur de requête de préfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères &quot;&amp;&quot;.

Permet de modifier en permanence les images et de stocker le corps des modèles.

Les commandes de ce champ sont remplacées par les mêmes commandes dans la requête ou le modèle à partir duquel cet enregistrement est référencé, ainsi que par les commandes de `catalog::PostModifier`

Les macros sont autorisées dans `catalog::Modifier`, à condition qu’elles soient définies dans le même catalogue ou dans le catalogue par défaut. Vous pouvez également utiliser des variables personnalisées.

## Propriétés {#section-6674388f77d644469371a17e8809c45f}

Chaîne de texte. Facultatif.

## Par défaut {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Aucune

## Voir aussi {#section-7a67803d141b442180c418c1f3cff029}

[catalogue::PostModificateur](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
