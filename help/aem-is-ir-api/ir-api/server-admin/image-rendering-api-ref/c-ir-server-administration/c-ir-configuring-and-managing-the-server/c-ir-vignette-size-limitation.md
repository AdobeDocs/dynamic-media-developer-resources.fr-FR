---
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-title: Limite de taille de vignette
solution: Experience Manager
title: Limite de taille de vignette
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Limite de taille de vignette{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [ !DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application requiert la prise en charge de vignettes non pyramidales dont la zone d’image (largeur x hauteur) est supérieure à cette limite.

>[!NOTE]
>
>`attribute::MaxPix` Il `IS::MaxMessageSize` peut également être nécessaire d’ajuster les images pour leur permettre de répondre à des tailles d’image exceptionnellement élevées. Pour plus d’informations, reportez-vous à la documentation sur la diffusion d’images.

