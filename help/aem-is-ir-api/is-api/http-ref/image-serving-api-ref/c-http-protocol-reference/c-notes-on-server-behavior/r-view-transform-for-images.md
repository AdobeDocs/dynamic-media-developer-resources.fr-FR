---
description: Transformation d’affichage pour les images
solution: Experience Manager
title: Transformation d’affichage pour les images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Transformation d’affichage pour les images{#view-transform-for-images}

L’image renvoyée au client en réponse à une `req=img` La demande est dérivée de l’image composite en prenant en compte les valeurs suivantes : `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`et la taille de l’image composite.

If `wid=` et `hei=` sont spécifiés, et `scl=` n’est pas défini, l’image composite est mise à l’échelle de sorte qu’elle s’adapte entièrement à l’état d’affichage défini par `wid=` et `hei=`. Si le rapport L/H de l’affichage rect est différent de celui de l’image composite, l’image composite mise à l’échelle est alignée dans l’affichage rect à l’aide de la propriété `align=` , si spécifié, ou centré dans le cas contraire. Tout espace non couvert par les données d’image est rempli de `bgc=` ou, le cas échéant, avec `attribute::BkgColor`.

If `scl=` est spécifié, l’image composite est mise à l’échelle selon ce facteur d’échelle. If `wid=` et/ou `hei=` est également spécifié, l’image mise à l’échelle est ensuite recadrée sur `wid=` et/ou `hei=` ou un espace supplémentaire est ajouté, si nécessaire. `align=` indique l’emplacement où l’image est recadrée ou où un espace supplémentaire est ajouté, et tout espace supplémentaire est rempli avec `bgc=` ou `attribute::BkgColor`.

Si aucun `wid=`, `hei=` nor `scl=` sont spécifiées et si la largeur ou la hauteur de l’image composite dépasse `attribute::DefaultPix`, l’image composite est mise à l’échelle de manière à ne pas dépasser `attribute::DefaultPix`. Sinon, l’image composite est utilisée sans mise à l’échelle.

Pour garantir que l’image d’affichage est renvoyée sans autre mise à l’échelle, spécifiez `scl=1`.

If `rgn=` est spécifiée, l’image de réponse est alors recadrée en conséquence pour obtenir la taille de l’image de réponse finale. Cette taille est comparée à `attribute::MaxPix` (s’il est défini) et une erreur est générée si l’image de réponse est plus grande dans l’une ou l’autre dimension.

If `fmt=` indique les données sans couche alpha, toutes les zones transparentes de l’image de réponse sont remplies avec `bgc=` ou `attribute::BkgColor`.
