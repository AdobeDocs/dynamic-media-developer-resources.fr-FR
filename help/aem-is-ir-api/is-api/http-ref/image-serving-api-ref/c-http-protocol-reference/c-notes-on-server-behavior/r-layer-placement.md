---
description: Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.
solution: Experience Manager
title: Emplacement des calques
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# Emplacement du calque{#layer-placement}

Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan à un décalage spécifié par pos=.

Si l’origine de calque n’est pas explicitement spécifiée pour un calque d’image, elle est calculée comme suit :

1. Déterminez l’ancrage de l’image. Utilisez `anchor=` ou, si ce n&#39;est pas spécifié, `catalog::Anchor`.
1. Si l’ancre d’image est définie, appliquez les transformations du calque et `extend=` pour le convertir en valeur origine=.
1. Si aucun ancrage d’image n’est défini, l’origine du calque est placée au centre du rectangle du calque (après avoir appliqué `extend=`).

![](assets/layerplacement.png)

