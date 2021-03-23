---
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-title: Limite de taille de vignette
solution: Experience Manager
title: Limite de taille de vignette
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Limite de taille de vignette{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [ !DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application requiert la prise en charge de vignettes non pyramidales dont la zone d’image (largeur x hauteur) est supérieure à cette limite.

>[!NOTE]
>
>`attribute::MaxPix` Il  `IS::MaxMessageSize` peut également s’avérer nécessaire d’ajuster la taille des images de réponse aux dimensions exceptionnellement élevées. Pour plus d’informations, reportez-vous à la documentation sur la diffusion d’images.

