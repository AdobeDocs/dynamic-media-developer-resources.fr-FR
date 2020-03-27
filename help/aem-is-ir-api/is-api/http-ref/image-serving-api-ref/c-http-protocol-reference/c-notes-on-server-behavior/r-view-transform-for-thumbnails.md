---
description: 'L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.'
seo-description: 'L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.'
seo-title: ' de transformation pour les miniatures'
solution: Experience Manager
title: ' de transformation pour les miniatures'
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


#  de transformation pour les miniatures{#view-transform-for-thumbnails}

L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute::DefaultThumbPix et attribute::MaxPix.

1. **Calculez le  rect** - Utilisez `wid=` ou la valeur de largeur `attribute::DefaultThumbPix` pour la largeur du  rect de. Utilisez `hei=` ou la valeur de hauteur de `attribute::DefaultThumbPix` pour la hauteur. Le  rect du doit être entièrement spécifié dans cette étape. (Notez que le  rect du sera le même que le rect du calque 0, si aucun n’ `size=`est spécifié pour le calque 0).
1. **Echelle le composite** - Si `catalog::ThumbType=Crop`, le composite est mis à l&#39;échelle à la plus petite image possible tout en remplissant l&#39;ensemble du  rect du ; les données d’image supplémentaires sont tronquées. Si `catalog::ThumbType= Fit`le composite est mis à l’échelle avec la plus grande image possible tout en ajustant l’ensemble du composite dans le  rect du. Si `catalog::ThumbType=Texture`le composite n’est pas mis à l’échelle du tout pour conserver la résolution spécifiée dans `catalog::ThumbRes`.
1. **Remplissage et recadrage** : le rectangle de  est rempli avec la `bgc=` couleur (ou, s’il n’est pas spécifié, avec `attribute::ThumbBkgColor`). Le composite mis à l’échelle est aligné sur  rect à l’aide de l’attribut : et attribut `ThumbHorizAlign` : `ThumbVertAlign`. Le composite mis à l’échelle est ensuite fusionné avec le  rect plein sans autre mise à l’échelle. Toutes les zones du composite qui s’étendent au-delà du rect de  sont coupées.

