---
description: La deuxième étape de la transformation du calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).
seo-description: La deuxième étape de la transformation du calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).
seo-title: Mise à l’échelle des miniatures
solution: Experience Manager
title: Mise à l’échelle des miniatures
topic: Dynamic Media Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Mise à l’échelle des miniatures{#thumbnail-scaling}

La deuxième étape de la transformation du calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).

* `2.` Si  `size=` vous le souhaitez, ajustez l’image (recadrée) dans le  `size=` rect à l’aide des règles de miniature. Si `size=` n&#39;est pas spécifié, effectuez une mise à l&#39;échelle basée sur `res=` ou, si `res=` n&#39;est pas spécifié, insérez l&#39;image (recadrée) dans le rect de trame à l&#39;aide des règles de miniature décrites ci-dessous.

