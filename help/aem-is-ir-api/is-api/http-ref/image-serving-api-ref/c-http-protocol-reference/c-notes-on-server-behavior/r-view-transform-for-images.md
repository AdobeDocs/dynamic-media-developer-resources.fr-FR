---
description: 'null'
seo-description: 'null'
seo-title: ' de transformation pour les images'
solution: Experience Manager
title: ' de transformation pour les images'
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  de transformation pour les images{#view-transform-for-images}

L’image renvoyée au client en réponse à une `req=img` demande est dérivée de l’image composite en prenant en compte les valeurs suivantes : `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`et la taille de l’image composite.

Si `wid=` et `hei=` sont spécifiés, et non `scl=` , l’image composite est mise à l’échelle de sorte qu’elle s’adapte parfaitement au  rect du défini par `wid=` et `hei=`. Si les proportions du  rect de l’sont différentes de celles de l’image composite, l’image composite redimensionnée est alignée dans le  rect de l’à l’aide de la `align=` valeur, le cas échéant, ou centrée autrement. Tout espace non couvert par les données d’image est rempli avec `bgc=` ou, s’il n’est pas spécifié, avec `attribute::BkgColor`.

Si `scl=` est spécifié, l’image composite est mise à l’échelle selon ce facteur d’échelle. Si `wid=` et/ou `hei=` est également spécifié, l’image mise à l’échelle est recadrée `wid=` (ou) et/ou `hei=` (ou) un espace supplémentaire est ajouté, selon les besoins. `align=` indique où l’image est recadrée ou où un espace supplémentaire est ajouté, et où tout espace supplémentaire est rempli avec `bgc=` ou `attribute::BkgColor`.

Si aucune `wid=`, `hei=` ni `scl=` n’est spécifiée et si la largeur ou la hauteur de l’image composite est supérieure `attribute::DefaultPix`, l’image composite est mise à l’échelle de manière à ne pas dépasser `attribute::DefaultPix`. Sinon, l’image composite est utilisée sans mise à l’échelle.

Pour vous assurer que l’image du  est renvoyée sans autre mise à l’échelle, spécifiez `scl=1`.

Si `rgn=` est spécifié, l’image de réponse est alors recadrée en conséquence pour obtenir la taille de l’image de réponse finale. Cette taille est comparée à `attribute::MaxPix` (si elle est définie) et une erreur est générée si l’image de réponse est plus grande dans l’une ou l’autre dimension.

Si `fmt=` spécifie des données sans alpha, toutes les zones transparentes de l’image de réponse sont remplies avec `bgc=` ou `attribute::BkgColor`.
