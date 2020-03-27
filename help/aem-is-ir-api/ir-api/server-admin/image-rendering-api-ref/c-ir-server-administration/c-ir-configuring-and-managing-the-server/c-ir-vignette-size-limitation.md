---
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
seo-title: Limite de taille du vignette
solution: Experience Manager
title: Limite de taille du vignette
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Limite de taille du vignette{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application requiert la prise en charge de vignettes non pyramidales avec une zone d’image (largeur x hauteur) supérieure à cette limite.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>`attribute::MaxPix` Il `IS::MaxMessageSize` peut également s’avérer nécessaire de l’ajuster pour permettre des tailles d’image de réponse exceptionnellement grandes. Pour plus d’informations, reportez-vous à la documentation de la diffusion d’images.

