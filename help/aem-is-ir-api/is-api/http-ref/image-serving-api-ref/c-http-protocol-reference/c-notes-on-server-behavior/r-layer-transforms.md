---
description: Les transformations sont appliquées aux images source et aux calques de texte.
seo-description: Les transformations sont appliquées aux images source et aux calques de texte.
seo-title: Transformations de calque
solution: Experience Manager
title: Transformations de calque
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Transformations de calque{#layer-transforms}

Les transformations sont appliquées aux images source et aux calques de texte.

Les opérations suivantes sont appliquées aux images source, dans l’ordre indiqué, pour obtenir la relation spatiale souhaitée avec la couche 0 :

1. Appliquer `crop=`, le cas échéant.
1. Echelle basée sur `size=` ou, si `size=` n’est pas spécifié, basée sur `scale=`ou, si `scale=` n’est pas spécifié, basée sur `res=``res=`ou, si non spécifié, utiliser l’image source à résolution totale.
1. Appliquer `flip=`, le cas échéant.
1. Appliquer `rotate=`, le cas échéant.
1. Appliquer `extend=`, le cas échéant.
1. Positionnez le calque dans la zone de travail en fonction `origin=` et `pos=` (voir ci-dessous).

Les transformations suivantes sont appliquées aux calques de texte :

1. La taille de la zone de texte est déterminée par `size=`, ou par la largeur et la hauteur du texte, si `size=` elle n’est fournie que partiellement ou pas du tout. Le texte est aligné dans la zone de texte à l’aide des attributs d’alignement du texte rtf. Le texte peut être recadré par la zone de texte.
1. Mettez à l’échelle le contenu du texte en fonction de la résolution spécifiée par `textAttr=`.
1. Appliquer `rotate=`, le cas échéant.
1. Appliquer `extend=`, le cas échéant.
1. Positionnez le calque dans la zone de travail en fonction `origin=` et `pos=`(voir ci-dessous).

Pour les calques d’image et de texte, le positionnement à la dernière étape du calque dans la zone de travail ne s’applique pas au calque 0, car le calque 0 constitue effectivement la zone de travail.
