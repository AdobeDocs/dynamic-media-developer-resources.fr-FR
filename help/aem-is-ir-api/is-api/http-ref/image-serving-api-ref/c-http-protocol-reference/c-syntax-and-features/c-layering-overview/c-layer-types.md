---
description: Quatre types de calques sont pris en charge.
solution: Experience Manager
title: Types de calques
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Types de calques{#layer-types}

Quatre types de calques sont pris en charge.

## Calques d’image {#section-3e53df1437694272aca03f927fc0db07}

Les calques d’image doivent avoir une commande `src=` qui spécifie l’image à utiliser comme calque. Une image distincte peut être spécifiée avec `mask=` à utiliser comme masque de calque ou l&#39;image peut avoir déjà un canal alpha. La taille des calques d’image est toujours dérivée de l’image, mais l’image est souvent mise à l’échelle pour s’ajuster à l’aide de la commande `size=`. Un chemin d&#39;accès à l&#39;élément peut être appliqué avec `clipPath=`.

## Calques de texte {#section-dc2aec6416a340bcb20c1f884323c8d0}

Doit comporter une commande `text=` ou `textPs=` qui fournit le contenu du texte sous la forme d’un fragment de texte au format RTF (Rich Text Format). Les calques de texte peuvent être redimensionnés automatiquement à leur contenu, ou peuvent se voir attribuer des tailles explicites (par exemple, si le texte doit être entouré d’une largeur spécifique ou si le texte doit être limité dans une zone spécifique). `textPs=` prise en charge de flux de texte en formes arbitraires définies avec  `textFlowPath=` et sur des chemins arbitraires définis avec  `textPath=`. `textPs=` prend également en charge le rendu du texte dans la zone de texte ou la forme spécifiée à des angles arbitraires (  `textAngle=`).

## Calques de couleur unie {#section-56dfb672756643dda08dc93294809eb0}

Les calques de couleur unie sont souvent utilisés pour le calque 0 dans les modèles, de sorte que la taille de l’image composite soit fixe et indépendante de tout contenu d’image. Les calques de couleur unie nécessitent un attribut `color=` et `size=` ou `mask=` et prennent en charge la plupart des autres commandes et attributs pour modifier l’aspect. Les couches de couleur unie peuvent recevoir des formes arbitraires avec `clipPath=`.

## Calques d’effets {#section-dd3b628bc6734077af4c0ddcebcee05f}

Les effets de calque de style Photoshop, tels que les ombres portées et les effets d’éclat, sont mis en oeuvre par IS à l’aide de sous-calques spéciaux qui peuvent être joints à des calques d’image, de texte et de couleur unie. Ces calques d’effets héritent du masque de calque parent et de la position du calque parent et sont limités en fonctionnalités.
