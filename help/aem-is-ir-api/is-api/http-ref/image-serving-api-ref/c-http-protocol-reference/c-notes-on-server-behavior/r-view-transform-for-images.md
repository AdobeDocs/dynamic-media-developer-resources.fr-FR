---
description: Transformation de la vue pour les images
solution: Experience Manager
title: Transformation de la vue pour les images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Transformation de la vue pour les images{#view-transform-for-images}

L’image renvoyée au client en réponse à une demande de `req=img` est dérivée de l’image composite en tenant compte des valeurs suivantes : `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` et la taille de l’image composite.

Si `wid=` et `hei=` sont spécifiés, mais `scl=` ne l’est pas, l’image composite est mise à l’échelle de sorte qu’elle s’adapte entièrement à la vue droite définie par `wid=` et `hei=`. Si le rapport d’aspect de la vue recte est différent de celui de l’image composite, l’image composite mise à l’échelle est alignée dans la vue recte à l’aide de la valeur de `align=`, si elle est spécifiée, ou elle est centrée dans le cas contraire. Tout espace non couvert par les données d’image est rempli de `bgc=` ou, s’il n’est pas spécifié, de `attribute::BkgColor`.

Si `scl=` est spécifié, l’image composite est mise à l’échelle selon ce facteur d’échelle. Si des `wid=` et/ou des `hei=` sont également spécifiés, l’image mise à l’échelle est ensuite recadrée en `wid=` et/ou un espace `hei=` ou supplémentaire est ajouté, si nécessaire. `align=` indique l’emplacement où l’image est recadrée ou un espace supplémentaire est ajouté, et tout espace supplémentaire est rempli de `bgc=` ou de `attribute::BkgColor`.

Si ni `wid=`, `hei=` ou `scl=` ne sont spécifiés, et si la largeur ou la hauteur de l’image composite dépasse `attribute::DefaultPix`, l’image composite est mise à l’échelle de manière à ne pas dépasser `attribute::DefaultPix`. Dans le cas contraire, l’image composite est utilisée sans mise à l’échelle.

Pour garantir que l’image d’affichage est renvoyée sans autre mise à l’échelle, spécifiez `scl=1`.

Si `rgn=` est spécifié, l’image de réponse est ensuite recadrée en conséquence pour obtenir la taille finale de l’image de réponse. Cette taille est comparée à `attribute::MaxPix` (si elle est définie) et une erreur est générée si l’image de réponse est plus grande dans l’une des dimensions.

Si `fmt=` spécifie des données sans couche alpha, toutes les zones transparentes de l’image de réponse sont remplies de `bgc=` ou de `attribute::BkgColor`.
