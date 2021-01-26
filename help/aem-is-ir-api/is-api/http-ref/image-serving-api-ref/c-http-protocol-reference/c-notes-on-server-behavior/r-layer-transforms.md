---
description: Les transformations sont appliquées aux images source et aux calques de texte.
seo-description: Les transformations sont appliquées aux images source et aux calques de texte.
seo-title: Transformations de calques
solution: Experience Manager
title: Transformations de calques
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Transformations de calque{#layer-transforms}

Les transformations sont appliquées aux images source et aux calques de texte.

Les opérations suivantes sont appliquées aux images source, dans l’ordre indiqué, pour obtenir la relation spatiale souhaitée avec la couche 0 :

1. Appliquez `crop=`, le cas échéant.
1. Échelle basée sur `size=` ou, si `size=` n&#39;est pas spécifié, sur `scale=`, ou, si `scale=` n&#39;est pas spécifié, sur `res=`, ou si `res=`n&#39;est pas spécifié, utilisez l&#39;image source à résolution complète.
1. Appliquez `flip=`, le cas échéant.
1. Appliquez `rotate=`, le cas échéant.
1. Appliquez `extend=`, le cas échéant.
1. Positionnez le calque dans la zone de travail en fonction de `origin=` et `pos=` (voir ci-dessous).

Les transformations suivantes s’appliquent aux calques de texte :

1. La taille de la zone de texte est déterminée par `size=`, ou par la largeur et la hauteur du texte, si `size=` n’est fourni que partiellement ou pas du tout. Le texte est aligné dans la zone de texte à l’aide des attributs d’alignement de texte rtf. Le texte peut être recadré par la zone de texte.
1. Mettez à l’échelle le contenu du texte en fonction de la résolution spécifiée par `textAttr=`.
1. Appliquez `rotate=`, le cas échéant.
1. Appliquez `extend=`, le cas échéant.
1. Positionnez le calque dans la zone de travail en fonction de `origin=` et `pos=` (voir ci-dessous).

Pour les calques d’image et de texte, la dernière étape de positionnement du calque dans la zone de travail ne s’applique pas au calque 0, car le calque 0 constitue effectivement la zone de travail.
