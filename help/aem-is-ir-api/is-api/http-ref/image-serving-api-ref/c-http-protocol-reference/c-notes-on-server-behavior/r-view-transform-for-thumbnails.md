---
description: L’image renvoyée au client en réponse à une requête req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.
solution: Experience Manager
title: Transformation d’affichage pour les miniatures
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Transformation d’affichage pour les miniatures{#view-transform-for-thumbnails}

L’image renvoyée au client en réponse à une demande req=tmb est dérivée de l’image composite en prenant en compte les valeurs suivantes : wid=, hei=, attribute::DefaultThumbPix, et attribute::MaxPix.

1. **Calcul du rect d’affichage**  : utilisez  `wid=` ou la valeur de largeur  `attribute::DefaultThumbPix` pour la largeur du rect d’affichage. Utilisez `hei=` ou la valeur de hauteur `attribute::DefaultThumbPix` pour la hauteur. L’affichage rect doit être entièrement spécifié dans cette étape. (Notez que la vue rect sera identique à la couche 0 rect, si aucun `size=`n’est spécifié pour la couche 0).
1. **Mise à l’échelle du composite**  : si  `catalog::ThumbType=Crop`, le composite est mis à l’échelle à la plus petite image possible tout en remplissant l’intégralité de l’affichage recto ; les données d’image supplémentaires sont tronquées. Si `catalog::ThumbType= Fit`, le composite est mis à l’échelle à la plus grande image possible tout en ajustant l’ensemble du composite dans la vue rect. Si `catalog::ThumbType=Texture`, le composite n’est pas mis à l’échelle du tout pour conserver la résolution spécifiée dans `catalog::ThumbRes`.
1. **Remplir et recadrer**  : la recette de la vue est remplie avec la  `bgc=` couleur (ou, si elle n’est pas spécifiée, avec  `attribute::ThumbBkgColor`). Le composite à mise à l’échelle est aligné avec le rect de vue à l’aide de l’attribut : `ThumbHorizAlign` et attribut : `ThumbVertAlign`. Le composite à mise à l’échelle est ensuite fusionné avec la recette d’affichage remplie sans autre mise à l’échelle. Toutes les zones du composite qui s’étendent au-delà de l’état d’affichage sont tronquées.
