---
description: Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.
seo-description: Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.
seo-title: Emplacement des calques
solution: Experience Manager
title: Emplacement des calques
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Emplacement du calque{#layer-placement}

Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.

Si l’origine de calque n’est pas explicitement spécifiée pour un calque d’image, elle est calculée comme suit :

1. Déterminez l’ancrage de l’image. Utilisez `anchor=` ou, si ce n&#39;est pas spécifié, `catalog::Anchor`.
1. Si l’ancre d’image est définie, appliquez les transformations du calque et `extend=` pour le convertir en valeur origine=.
1. Si aucun ancrage d’image n’est défini, l’origine du calque est placée au centre du rectangle du calque (après avoir appliqué `extend=`).

![](assets/layerplacement.png)

