---
description: Les calques sont positionnés en alignant l’origine du calque (origin=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.
solution: Experience Manager
title: Emplacement des calques
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Emplacement des calques{#layer-placement}

Les calques sont positionnés en alignant l’origine du calque (origin=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.

Si l’origine du calque n’est pas spécifiée explicitement pour un calque d’image, elle est calculée comme suit :

1. Déterminez l’ancre de l’image. Utilisez `anchor=` ou, si non spécifié, `catalog::Anchor`.
1. Si l’ancre de l’image est définie, appliquez les transformations de calque et `extend=` pour la convertir en valeur origin=.
1. Si aucune ancre d’image n’est définie, l’origine du calque est placée au centre du rectangle du calque (après avoir appliqué `extend=`).

![](assets/layerplacement.png)
