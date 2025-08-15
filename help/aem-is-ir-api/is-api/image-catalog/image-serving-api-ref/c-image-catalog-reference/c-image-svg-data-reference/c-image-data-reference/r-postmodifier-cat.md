---
description: Chaîne de modificateur de demande postfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères « & ».
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Chaîne de modificateur de demande postfixe. Aucune ou plusieurs commandes de diffusion d’images séparées par des caractères « &amp; ».

Les commandes de ce champ remplacent toujours les commandes de la requête HTTP et du fichier `catalog::Modifier`.

`catalog::PostModifier` est utile si certaines images nécessitent des paramètres spéciaux qui sont normalement contrôlés à partir de l’URL, tels que `qlt=` ou `resmode=`. `catalog::Modifier` doit être utilisée pour définir la plupart des commandes IS du catalogue d’images.

Les macros sont autorisées dans `catalog::PostModifier`, à condition qu’elles soient définies dans le même catalogue ou dans le catalogue par défaut. Des variables personnalisées peuvent également être utilisées.

>[!NOTE]
>
>Si une demande implique plusieurs calques, seul le contenu du `catalog::PostModifier` calque 0 est appliqué. `catalog::PostModifier` de toutes les autres couches est ignorée.

## Propriétés {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Chaîne de texte. Facultatif.

## Par défaut {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Aucune

## Voir aussi {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog ::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
