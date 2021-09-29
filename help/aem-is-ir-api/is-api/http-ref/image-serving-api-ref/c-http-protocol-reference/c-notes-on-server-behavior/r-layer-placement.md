---
title: Emplacement des calques
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Emplacement des calques{#layer-placement}

Les calques sont positionnés en alignant l’origine du calque (origin=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.

Si l’origine du calque n’est pas spécifiée explicitement pour un calque d’image, elle est calculée comme suit :

1. Déterminez l’ancre de l’image. Utilisez `anchor=` ou, si non spécifié, `catalog::Anchor`.
1. Si l’ancre de l’image est définie, appliquez les transformations de calque et `extend=` pour la convertir en valeur origin=.
1. Si aucune ancre d’image n’est définie, l’origine du calque est placée au centre du rectangle du calque (après avoir appliqué `extend=`).

![Image de placement de calque](assets/layerplacement.png)
