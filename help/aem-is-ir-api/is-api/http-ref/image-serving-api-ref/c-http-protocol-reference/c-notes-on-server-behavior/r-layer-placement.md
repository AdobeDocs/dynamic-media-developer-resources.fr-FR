---
title: Placement des calques
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# Placement des calques{#layer-placement}

Les calques sont positionnés en alignant l’origine du calque (origine=) avec l’origine du calque d’arrière-plan selon un décalage spécifié par pos=.

Si l’origine du calque n’est pas spécifiée explicitement pour un calque d’image, elle est calculée comme suit :

1. Déterminez l’ancre d’image. Utilisez `anchor=` ou, si ce n’est pas spécifié, `catalog::Anchor`.
1. Si l’ancre d’image est définie, appliquez les transformations de calque et `extend=` pour la convertir en valeur origin= .
1. Si aucune ancre d’image n’est définie, l’origine du calque est placée au centre du rectangle du calque (après application de `extend=`).

![Image d’emplacement du calque](assets/layerplacement.png)
