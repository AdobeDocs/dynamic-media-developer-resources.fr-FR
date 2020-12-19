---
description: 'L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.'
seo-description: 'L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.'
seo-title: Transformation de la vue pour les miniatures
solution: Experience Manager
title: Transformation de la vue pour les miniatures
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Transformation de vue pour les miniatures{#view-transform-for-thumbnails}

L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute::DefaultThumbPix et attribute::MaxPix.

1. **Calculer la recette**  de la vue - Utiliser  `wid=` ou la valeur de largeur  `attribute::DefaultThumbPix` pour la largeur de la recette de la vue. Utilisez `hei=` ou la valeur de hauteur `attribute::DefaultThumbPix` pour la hauteur. La recette de la vue doit être entièrement spécifiée dans cette étape. (Notez que la rect de vue sera identique à la rect de calque 0, si aucun `size=`n’est spécifié pour la couche 0).
1. **Mettre à l&#39;échelle le composite**  - Si  `catalog::ThumbType=Crop`le composite est mis à l&#39;échelle avec la plus petite image possible tout en remplissant la totalité de la recette de vue ; les données d’image supplémentaires sont tronquées. Si `catalog::ThumbType= Fit`, le composite est mis à l’échelle avec la plus grande image possible tout en ajustant l’ensemble du composite dans la recette de vue. Si `catalog::ThumbType=Texture`, le composite n&#39;est pas mis à l&#39;échelle du tout pour conserver la résolution spécifiée dans `catalog::ThumbRes`.
1. **Remplissage et recadrage**  : la recette de la vue est remplie avec la  `bgc=` couleur (ou, si elle n&#39;est pas spécifiée, avec  `attribute::ThumbBkgColor`). Le composite mis à l’échelle est aligné avec la recette de vue à l’aide de l’attribut : `ThumbHorizAlign` et attribut : `ThumbVertAlign`. Le composite mis à l’échelle est ensuite fusionné avec la recette de vue remplie sans autre mise à l’échelle. Toutes les zones du composite qui s’étendent au-delà de la limite de vue sont découpées.

