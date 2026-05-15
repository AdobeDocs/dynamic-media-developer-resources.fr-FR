---
description: Chaîne de modificateur de requête de suffixe. Aucune ou plusieurs commandes de traitement d’images séparées par des caractères «& ».
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
TQID: 'https://experienceleague.adobe.com/hPHoHlBkRN-eXFvLzZ2LpWhmtiT4lGyehTvwFw9ItJo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 3%

---

# PostModifier{#postmodifier}

Chaîne de modificateur de requête de suffixe. Aucune ou plusieurs commandes de traitement d’images séparées par des caractères «&amp; ».

Les commandes de ce champ remplacent toujours les commandes de la requête HTTP et dans `catalog::Modifier`.

`catalog::PostModifier` est utile si certaines images nécessitent des paramètres spéciaux qui sont normalement contrôlés à partir de l’URL, tels que `qlt=` ou `resmode=`. `catalog::Modifier` doit être utilisé pour définir la plupart des commandes IS dans le catalogue d’images.

Les macros sont autorisées dans `catalog::PostModifier`, à condition qu’elles soient définies dans le même catalogue ou dans le catalogue par défaut. Des variables personnalisées peuvent également être utilisées.

>[!NOTE]
>
>Si une requête implique plusieurs calques, seul le contenu du `catalog::PostModifier` du calque 0 est appliqué. `catalog::PostModifier` de tous les autres calques est ignoré.

## Propriétés {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Chaîne de texte. Facultatif.

## Par défaut {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Aucune

## Voir aussi {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
