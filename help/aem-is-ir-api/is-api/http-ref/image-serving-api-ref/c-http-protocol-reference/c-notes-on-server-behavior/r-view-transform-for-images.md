---
description: Transformation d’affichage pour les images
solution: Experience Manager
title: Transformation d’affichage pour les images
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Transformation d’affichage pour les images{#view-transform-for-images}

L’image renvoyée au client en réponse à une demande `req=img` est dérivée de l’image composite en prenant en compte les valeurs suivantes : `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` et la taille de l’image composite.

Si `wid=` et `hei=` sont spécifiés, et que `scl=` ne l’est pas, l’image composite est mise à l’échelle de sorte qu’elle s’adapte entièrement à l’affichage rect défini par `wid=` et `hei=`. Si le rapport L/H de l’affichage rect est différent de celui de l’image composite, l’image composite redimensionnée est alignée dans l’affichage rect à l’aide de la valeur `align=` , si elle est spécifiée, ou elle est centrée dans le cas contraire. Tout espace non couvert par les données d’image est rempli de `bgc=` ou, s’il n’est pas spécifié, de `attribute::BkgColor`.

Si `scl=` est spécifié, l’image composite est mise à l’échelle selon ce facteur d’échelle. Si `wid=` et/ou `hei=` est également spécifié, l’image mise à l’échelle est ensuite recadrée sur `wid=` et/ou `hei=` ou un espace supplémentaire est ajouté, si nécessaire. `align=` indique l’emplacement où l’image est recadrée ou où un espace supplémentaire est ajouté, et tout espace supplémentaire est rempli avec  `bgc=` ou  `attribute::BkgColor`.

Si aucun `wid=`, `hei=` ou `scl=` n’est spécifié et si la largeur ou la hauteur de l’image composite dépasse `attribute::DefaultPix`, l’image composite est mise à l’échelle de façon à ne pas dépasser `attribute::DefaultPix`. Sinon, l’image composite est utilisée sans mise à l’échelle.

Pour garantir que l’image de la vue est renvoyée sans autre mise à l’échelle, spécifiez `scl=1`.

Si `rgn=` est spécifié, l’image de réponse est recadrée en conséquence pour obtenir la taille de l’image de réponse finale. Cette taille est comparée à `attribute::MaxPix` (si définie) et une erreur est générée si l’image de réponse est plus grande dans l’une des dimensions.

Si `fmt=` indique des données sans couche alpha, toutes les zones transparentes de l’image de réponse sont remplies par `bgc=` ou `attribute::BkgColor`.
