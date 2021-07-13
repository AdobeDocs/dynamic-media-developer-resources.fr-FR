---
description: Quatre types de calques sont pris en charge.
solution: Experience Manager
title: Types de calques
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Types de calques{#layer-types}

Quatre types de calques sont pris en charge.

## Calques d’image {#section-3e53df1437694272aca03f927fc0db07}

Les calques d’image doivent comporter une commande `src=` qui spécifie l’image à utiliser comme calque. Une image distincte peut être spécifiée avec `mask=` à utiliser comme masque de calque ou l’image peut déjà avoir un canal alpha. La taille des calques d’image est toujours dérivée de l’image, mais l’image est souvent mise à l’échelle pour s’adapter à l’aide de la commande `size=`. Un chemin de clip peut être appliqué avec `clipPath=`.

## Calques de texte {#section-dc2aec6416a340bcb20c1f884323c8d0}

Doit comporter une commande `text=` ou `textPs=` qui fournit le contenu texte sous la forme d’un fragment de texte au format texte enrichi (RTF). Les calques de texte peuvent être redimensionnés automatiquement en fonction de leur contenu ou peuvent se voir attribuer des tailles explicites (par exemple, si le texte doit être encapsulé sur une largeur spécifique ou si le texte doit être limité dans une zone spécifique). `textPs=` prise en charge du flux de texte en formes arbitraires définies avec  `textFlowPath=` et sur des chemins arbitraires définis avec  `textPath=`. `textPs=` prend également en charge le rendu du texte dans la zone de texte ou la forme spécifiée à des angles arbitraires (  `textAngle=`).

## Calques de couleur unie {#section-56dfb672756643dda08dc93294809eb0}

Les calques de couleur unie sont souvent utilisés pour le calque 0 dans les modèles, de sorte que la taille de l’image composite est fixe et indépendante de tout contenu d’image. Les calques de couleur unie requièrent un attribut `color=` et `size=` ou `mask=`. Ils prennent également en charge la plupart des autres commandes et attributs pour modifier l’aspect. Les calques de couleur unie peuvent recevoir des formes arbitraires avec `clipPath=`.

## Calques d’effet {#section-dd3b628bc6734077af4c0ddcebcee05f}

Les effets de calque de style Photoshop, tels que les ombres portées et les effets d’éclat, sont implémentés par IS à l’aide de sous-calques spéciaux pouvant être joints à l’image, au texte et aux calques de couleur unis. Ces calques d’effet héritent du masque de calque parent et de la position du calque parent et sont limités en fonctionnalité.
