---
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
solution: Experience Manager
title: Limite de taille de vignette
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Limite de taille de vignette{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [ !DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application requiert la prise en charge de vignettes non pyramidales dont la zone d’image (largeur x hauteur) est supérieure à cette limite.

>[!NOTE]
>
>`attribute::MaxPix` Il  `IS::MaxMessageSize` peut également s’avérer nécessaire d’ajuster la taille des images de réponse aux dimensions exceptionnellement élevées. Pour plus d’informations, reportez-vous à la documentation sur la diffusion d’images.

