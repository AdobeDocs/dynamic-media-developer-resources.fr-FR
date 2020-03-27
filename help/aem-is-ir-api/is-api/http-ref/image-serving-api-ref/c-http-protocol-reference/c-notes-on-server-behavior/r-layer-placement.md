---
description: Les calques sont positionnés en alignant le calque   ( =) avec le du calque d’arrière-plan à un décalage spécifié par pos=.
seo-description: Les calques sont positionnés en alignant le calque   ( =) avec le du calque d’arrière-plan à un décalage spécifié par pos=.
seo-title: Positionnement des calques
solution: Experience Manager
title: Positionnement des calques
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Positionnement des calques{#layer-placement}

Les calques sont positionnés en alignant le calque   ( =) avec le du calque d’arrière-plan à un décalage spécifié par pos=.

Si le calque   n’est pas spécifié explicitement pour un calque d’image, il est calculé comme suit :

1. Déterminez le point d’ancrage de l’image. Utilisez `anchor=`, ou, si ce n’est pas spécifié, `catalog::Anchor`.
1. Si l’ancre de l’image est définie, appliquez les transformations du calque et `extend=` convertissez-le en valeur  =.
1. Si aucun ancrage d’image n’est défini, le calque  le  est placé au centre du rectangle du calque (après application `extend=`).

![](assets/layerplacement.png)

