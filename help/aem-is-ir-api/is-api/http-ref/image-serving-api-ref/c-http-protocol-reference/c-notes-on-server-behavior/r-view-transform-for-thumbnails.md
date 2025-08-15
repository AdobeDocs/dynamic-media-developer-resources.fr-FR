---
description: 'L’image renvoyée au client en réponse à une requête req=tmb est dérivée de l’image composite en tenant compte des valeurs suivantes : wid=, hei=, attribute DefaultThumbPix et attribute MaxPix.'
solution: Experience Manager
title: Transformation des vues pour les miniatures
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Transformation des vues pour les miniatures{#view-transform-for-thumbnails}

L’image renvoyée au client en réponse à une requête req=tmb est dérivée de l’image composite en tenant compte des valeurs suivantes : wid=, hei=, attribute::DefaultThumbPix et attribute::MaxPix.

1. **Calculer la vue recte** - Utilisez `wid=` ou la valeur de largeur de `attribute::DefaultThumbPix` pour la largeur de la vue recte. Utilisez `hei=` ou la valeur de hauteur de `attribute::DefaultThumbPix` pour la hauteur. Le rectangle de vue doit être entièrement spécifié au cours de cette étape. (Notez que la vue recte est identique à la vue recte du calque 0, si aucune `size=` n&#39;est spécifiée pour le calque 0).
1. **Mettre le composite à l’échelle** - Si `catalog::ThumbType=Crop`, le composite est mis à l’échelle à la plus petite image possible tout en remplissant tout le rectangle de vue ; les données d’image supplémentaires sont recadrées. Si `catalog::ThumbType= Fit`, le composite est mis à l’échelle à la plus grande image possible tout en adaptant l’ensemble du composite à la vue recette. Si `catalog::ThumbType=Texture`, le composite n’est pas mis à l’échelle du tout pour conserver la résolution spécifiée dans `catalog::ThumbRes`.
1. **Remplir et recadrer** - La vue recette est remplie avec la couleur `bgc=` (ou, si elle n’est pas spécifiée, avec `attribute::ThumbBkgColor`). Le composite mis à l&#39;échelle est aligné avec la vue rect en utilisant l&#39;attribut : `ThumbHorizAlign` et l&#39;attribut : `ThumbVertAlign`. Le composite mis à l’échelle est ensuite fusionné avec la vue remplie directement sans autre mise à l’échelle. Toutes les zones du composite qui s&#39;étendent au-delà de la vue recette sont recadrées.
