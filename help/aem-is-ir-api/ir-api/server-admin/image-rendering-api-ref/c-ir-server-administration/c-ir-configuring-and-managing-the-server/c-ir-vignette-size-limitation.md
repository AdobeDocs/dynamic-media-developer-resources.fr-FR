---
title: Limitation de la taille de la vignette
description: Le rendu d’image applique une limite de taille de deux mégapixels pour les vignettes non pyramidales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# Limitation de la taille de la vignette{#vignette-size-limitation}

Le rendu d’image applique une limite de taille de deux mégapixels pour les vignettes non pyramidales.

Modifiez la valeur de `IrMaxNonPyrVignetteSize` dans [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] si votre application nécessite la prise en charge de vignettes non pyramidales dont la zone d’image (largeur x hauteur) est supérieure à cette limite.

>[!NOTE]
>
>Ajustez les attributs `attribute::MaxPix` et `IS::MaxMessageSize` pour permettre des tailles d’image de réponse inhabituellement grandes. Consultez la documentation du service d’images pour plus d’informations.

