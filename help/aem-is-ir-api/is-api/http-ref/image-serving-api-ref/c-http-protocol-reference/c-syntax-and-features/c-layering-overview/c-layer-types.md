---
description: Quatre types de calques sont pris en charge.
solution: Experience Manager
title: Types de calques
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Types de calques{#layer-types}

Quatre types de calques sont pris en charge.

## Calques d’image {#section-3e53df1437694272aca03f927fc0db07}

Les calques d’image doivent comporter une commande `src=` qui spécifie l’image à utiliser comme calque. Une image distincte peut être spécifiée avec des `mask=` à utiliser comme masque de calque ou l’image peut déjà avoir un canal alpha. La taille des calques d’image est toujours dérivée de l’image, mais celle-ci est souvent mise à l’échelle pour s’adapter à l’aide de la commande `size=`. Vous pouvez appliquer une trajectoire d’élément à l’aide de `clipPath=`.

## Calques de texte {#section-dc2aec6416a340bcb20c1f884323c8d0}

Doit comporter une commande `text=` ou `textPs=` qui fournit le contenu textuel sous la forme d’un fragment de texte au format RTF (Rich-text-formatted). Les calques de texte peuvent être redimensionnés automatiquement en fonction de leur contenu ou recevoir des tailles explicites. Par exemple, si le texte doit être renvoyé à la ligne à une largeur spécifique ou si le texte doit être limité à une zone spécifique. `textPs=` prend en charge le transfert de texte dans des formes arbitraires définies avec `textFlowPath=` et sur des chemins arbitraires définis avec `textPath=`. `textPs=` prend également en charge le rendu de texte dans la zone de texte ou la forme spécifiée selon des angles arbitraires ( `textAngle=`).

## Calques de couleur unie {#section-56dfb672756643dda08dc93294809eb0}

Les calques de couleur unie sont souvent utilisés pour le calque 0 dans les modèles, de sorte que la taille de l’image composite est fixe et indépendante du contenu de l’image. Les calques de couleur unie nécessitent un attribut `color=`, `size=` ou `mask=`, et prennent en charge la plupart des autres commandes et attributs pour modifier l’aspect. Les calques de couleur unie peuvent prendre des formes arbitraires avec des `clipPath=`.

## Calques d’effet {#section-dd3b628bc6734077af4c0ddcebcee05f}

Les effets de calque de style Photoshop, tels que les ombres portées et les effets de lueur, sont implémentés par IS à l’aide de sous-calques spéciaux qui peuvent être associés à des calques d’image, de texte et de couleur unie. Ces calques d’effet héritent du masque de calque parent et de sa position, et leurs fonctionnalités sont limitées.
