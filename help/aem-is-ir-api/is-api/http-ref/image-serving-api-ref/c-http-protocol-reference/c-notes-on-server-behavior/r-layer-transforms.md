---
description: Les transformations sont appliquées aux images source et aux calques de texte.
solution: Experience Manager
title: Transformations de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Transformations de calque{#layer-transforms}

Les transformations sont appliquées aux images source et aux calques de texte.

Les opérations suivantes sont appliquées aux images sources, dans l’ordre donné, pour obtenir la relation spatiale souhaitée avec le calque 0 :

1. Appliquez `crop=`, si spécifié.
1. Mise à l’échelle en fonction de `size=` ou, si `size=` n’est pas spécifiée, en fonction de `scale=`, ou, si `scale=` n’est pas spécifiée, en fonction de `res=`ou, si `res=`n’est pas spécifiée, utilisez l’image source pleine résolution.
1. Appliquez `flip=`, si spécifié.
1. Appliquez `rotate=`, si spécifié.
1. Appliquez `extend=`, si spécifié.
1. Positionnez le calque dans la zone de travail en fonction de `origin=` et `pos=` (voir ci-dessous).

Les transformations suivantes sont appliquées aux calques de texte :

1. La taille de la zone de texte est déterminée par `size=`, ou la largeur et la hauteur du texte, si `size=` n’est que partiellement ou pas du tout fournie. Le texte est aligné dans la zone de texte à l’aide des attributs d’alignement de texte rtf. Le texte peut être rogné par la zone de texte.
1. Redimensionnez le contenu du texte en fonction de la résolution spécifiée avec `textAttr=`.
1. Appliquez `rotate=`, si spécifié.
1. Appliquez `extend=`, si spécifié.
1. Positionnez le calque dans la zone de travail en fonction de `origin=` et `pos=`(voir ci-dessous).

Pour les calques d’image et de texte, la dernière étape, à savoir le positionnement du calque dans la zone de travail, ne s’applique pas au calque 0, car le calque 0 constitue effectivement la zone de travail.
