---
title: Limitation de la taille des vignettes
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Limitation de la taille des vignettes{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application nécessite la prise en charge de vignettes non pyramidales avec une zone d’image (largeur x hauteur) supérieure à cette limite.

>[!NOTE]
>
>Ajustez les attributs `attribute::MaxPix` et `IS::MaxMessageSize` pour permettre des tailles d’image de réponse exceptionnellement grandes. Pour plus d’informations, reportez-vous à la documentation du serveur d’images .
