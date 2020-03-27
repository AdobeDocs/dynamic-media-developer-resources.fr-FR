---
description: Chaîne de modificateur de requête de suffixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères "&".
seo-description: Chaîne de modificateur de requête de suffixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères "&".
seo-title: PostModificateur
solution: Experience Manager
title: PostModificateur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModificateur{#postmodifier}

Chaîne de modificateur de requête de suffixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères &quot;&amp;&quot;.

Les commandes de ce champ remplacent toujours les commandes de la requête HTTP et de `catalog::Modifier`la commande dans.

`catalog::PostModifier` est utile si certaines images nécessitent des paramètres spéciaux qui sont normalement contrôlés à partir de l’URL, tels que `qlt=` ou `resmode=`. `catalog::Modifier` doit être utilisée pour définir la plupart des commandes IS dans le catalogue d’images.

Les macros sont autorisées dans `catalog::PostModifier`, à condition qu’elles soient définies dans le même catalogue ou dans le catalogue par défaut. Vous pouvez également utiliser des variables personnalisées.

>[!NOTE]
>
>Si une requête implique plusieurs calques, seul le contenu `catalog::PostModifier` du calque 0 est appliqué. `catalog::PostModifier` de tous les autres calques est ignoré.

## Propriétés {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Chaîne de texte. Facultatif.

## Par défaut {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Aucune

## Voir aussi {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalogue:Modificateur](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
