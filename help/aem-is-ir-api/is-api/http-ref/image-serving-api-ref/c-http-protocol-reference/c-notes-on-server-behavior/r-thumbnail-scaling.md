---
description: L’étape 2 du calque d’image est modifiée comme suit pour les miniatures (c.-à-d. si req=tmb).
seo-description: L’étape 2 du calque d’image est modifiée comme suit pour les miniatures (c.-à-d. si req=tmb).
seo-title: Mise à l’échelle des miniatures
solution: Experience Manager
title: Mise à l’échelle des miniatures
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# Mise à l’échelle des miniatures{#thumbnail-scaling}

L’étape 2 du calque d’image est modifiée comme suit pour les miniatures (c.-à-d. si req=tmb).

* `2.` Si `size=` est spécifié, ajustez l’image (recadrée) dans le `size=` rect à l’aide des règles de miniature. Si `size=` ce paramètre n’est pas spécifié, ajustez l’image (recadrée) en fonction `res=`ou, si `res=` elle n’est pas spécifiée, ajustez-la dans le rectangle de la zone de travail à l’aide des règles de miniature décrites ci-dessous.

