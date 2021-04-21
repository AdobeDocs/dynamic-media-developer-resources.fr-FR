---
description: Transformation de vue pour les images
solution: Experience Manager
title: Transformation de vue pour les images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Transformation de vue pour les images {#view-transform-for-images}

L’image renvoyée au client en réponse à une demande `req=img` est dérivée de l’image composite en prenant en compte les valeurs suivantes : `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` et la taille de l&#39;image composite.

Si `wid=` et `hei=` sont spécifiés, et `scl=` ne l’est pas, l’image composite est mise à l’échelle de sorte qu’elle s’adapte parfaitement à la vue définie par `wid=` et `hei=`. Si le rapport L/H de la recette de la vue est différent de celui de l’image composite, l’image composite mise à l’échelle est alignée dans la rect de la vue à l’aide de la valeur `align=`, si elle est spécifiée, ou elle est centrée autrement. Tout espace non couvert par les données d’image est rempli avec `bgc=` ou, s’il n’est pas spécifié, avec `attribute::BkgColor`.

Si `scl=` est spécifié, l’image composite est mise à l’échelle selon ce facteur d’échelle. Si `wid=` et/ou `hei=` est également spécifié, l’image mise à l’échelle est alors recadrée sur `wid=` et/ou `hei=` ou un espace supplémentaire est ajouté, si nécessaire. `align=` indique où l’image est recadrée ou où un espace supplémentaire est ajouté, et tout espace supplémentaire est rempli avec  `bgc=` ou  `attribute::BkgColor`.

Si aucun élément `wid=`, `hei=` ou `scl=` n&#39;est spécifié et si la largeur ou la hauteur de l&#39;image composite dépasse `attribute::DefaultPix`, l&#39;image composite est mise à l&#39;échelle pour ne pas dépasser `attribute::DefaultPix`. Sinon, l’image composite est utilisée sans mise à l’échelle.

Pour vous assurer que l’image de la vue est renvoyée sans autre mise à l’échelle, spécifiez `scl=1`.

Si `rgn=` est spécifié, l’image de réponse est alors recadrée en conséquence pour obtenir la taille d’image de réponse finale. Cette taille est comparée à `attribute::MaxPix` (si définie) et une erreur est générée si l’image de réponse est plus grande dans l’une ou l’autre dimension.

Si `fmt=` spécifie des données sans alpha, toutes les zones transparentes de l’image de réponse sont remplies avec `bgc=` ou `attribute::BkgColor`.
