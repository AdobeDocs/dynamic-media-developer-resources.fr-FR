---
description: Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.
solution: Experience Manager
title: Limitation de la taille des vignettes
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Limitation de la taille des vignettes{#vignette-size-limitation}

Le rendu d’image impose une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur `IrMaxNonPyrVignetteSize` dans [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application nécessite la prise en charge de vignettes non pyramidales avec une zone d’image (largeur x hauteur) supérieure à cette limite.

>[!NOTE]
>
>`attribute::MaxPix` et  `IS::MaxMessageSize` peuvent également devoir être ajustés pour permettre des tailles d’image de réponse exceptionnellement élevées. Pour plus d’informations, reportez-vous à la documentation du serveur d’images .
